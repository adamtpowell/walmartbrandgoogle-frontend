<template>
  <div class="home">
    <InfoBar />
    <Center>
      <Search />        
      <p class="legal">Note: these sites are sourced from openphish.com's phishing feed and UBlock origin's Spam404 list.
          While they are likely to be scams, they may not be.</p>
      <p class="legal">Also: This site only shows images of the allegedely malicious sites. It is safe to click on the links
          on our site. DO NOT visit the sites listed.</p>
    </Center>
  </div>
</template>

<script>
// @ is an alias to /src
import InfoBar from '@/components/InfoBar.vue'
import Center from '@/components/Center.vue'
import Search from '@/components/Search.vue'

export default {
  name: 'home',
  components: {
    InfoBar,
    Center,
    Search
  }
}
</script>
