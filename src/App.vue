<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>

:root {
    font-size: 30px;
}

*, *:after, *:before{
    font-family: walmart !important;
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 0;
}

@font-face {
    font-family: walmart;
    src: url("assets/font.ttf") format('truetype');
}
</style>