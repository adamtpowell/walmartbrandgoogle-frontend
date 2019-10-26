<template>
  <div class="outer">
    <div class="inner">
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfoBar'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.outer {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 95vh;
}

</style>
