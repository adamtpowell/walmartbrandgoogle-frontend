<template>
  <div>
    <Search :search="searchTerm" />
    <div v-if="results.length===0">
        <h3>No results found for {{searchTerm}}.</h3>
    </div>
    <SearchResult v-for="result in results" :key="result.url" :result="result" />
  </div>
</template>

<script>
// @ is an alias to /src
import Search from '@/components/Search.vue'
import SearchResult from '@/components/SearchResult.vue'

export default {
  name: 'home',
  components: {
    Search,
    SearchResult
  },
  data: function() {
    return {
      searchTerm: "",
      results: []
    }
  },
  methods: {
    updateSearch() {
      this.searchTerm = this.$route.query.q;
      fetch(`http://localhost:3000/searchapi?search=${this.searchTerm}`).then((res) => res.json()).then(json => {
          this.results = json.results;
      });
    }
  },
  watch: {
    $route() {
      this.updateSearch();
    }
  },
  mounted: function() {
    this.updateSearch();
  }
}
</script>
