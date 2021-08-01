<template>
  <div class="layout-wrapper">
    <Intro @removeIntro="intro = true" />
    <div class="content-wrapper">
      <LazyHeader v-if="intro" class="header" />
    </div>
    <LazyJobTitles v-if="intro" />
    <LazyHello v-if="intro" />
    <LazyProjects v-if="intro" />
    <LazyThanks v-if="intro" />
  </div>
</template>

<style scoped>
  .content-wrapper {
    display: grid;
    grid-template-columns: auto minmax(auto, 1440px) auto;
  }

  .header {
    grid-column: 2;
  }
</style>

<script>
  export default {
    data() {
      return {
        intro: false
      }
    }
  }
</script>
