<template>
  <form @submit.prevent="sendSearch()">
    <router-link to="/"><img src="logo.png" alt="Googel" style="width:100%; height: auto;"></router-link>
    <div class="searchbox-group">
        <input type="text" placeholder="Q" name="search" class="searchbox" v-model="searchTerm">
        <input type="submit" value="Search">
    </div>
  </form>
</template>

<script>
export default {
  name: 'Search',
  props: {
    "search": String
  },
  data() {
    return {
      searchTerm: ""
    }
  },
  methods: {
    sendSearch() {
      this.$router.push(`/search?q=${this.searchTerm}`)
    }
  },
  mounted: function() {
    this.searchTerm = this.$route.query.q;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



</style>
