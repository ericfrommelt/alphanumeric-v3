<template>
  <div class="layout-wrapper">
    <div class="content-wrapper">
      <Header class="header" />
    </div>
    <JobTitles />
    <Hello />
    <Projects />
    <Thanks />
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
