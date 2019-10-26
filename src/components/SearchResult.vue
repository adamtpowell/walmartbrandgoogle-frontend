<template>
  <div>
    <h3 v-on:click.self="modalShow(result.url, result.description)">{{result.url}}</h3>
    <p class="description">{{result.description}}</p>
  </div>
</template>

<script>
export default {
  name: 'InfoBar',
  props: {
    result: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
