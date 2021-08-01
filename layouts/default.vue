<template>
  <Nuxt />
</template>

<style>
  :root {
    --primary-color-dark: hsl(0 0% 16%);
    --primary-color-light: hsl(0 0% 100%);
  }

  html,
  body {
    background-color: var(--primary-color-light);
    color: var(--primary-color-dark);
    padding: 0;
    margin: 0;
    font-family: ibm-plex-sans, -apple-system, BlinkMacSystemFont, Segoe UI,
      Roboto, Oxygen, Ubuntu, Cantarell, Fira Sans, Droid Sans, Helvetica Neue,
      sans-serif;
    overflow-x: hidden;
  }

  img {
    max-width: 100%;
    height: auto;
  }

  a {
    color: inherit;
    text-decoration: none;
  }

  * {
    box-sizing: border-box;
  }

  figure {
    margin: 0;
  }

  video {
    width: 100% !important;
    height: auto !important;
  }

  .grid__wrapper {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
  }

  .section__block {
    width: 22px;
    height: 5px;
    background-color: #FF0005;
    grid-column: 2 / span 11;
  }

  @media(min-width: 900px) {
    .section__block {
      width: 44px;
      height: 10px;
    }
  }
</style>