<template>
  <section class="grid__wrapper thanks">
    <div class="section__block"></div>
    <p class="thanks__txt">
      Thanks for your time.<br />Let’s chat about how I can help.
    </p>
    <p class="thanks__txt">
      <span class="italic">Say hello—</span><br />
      <a href="mailto:eric@alphanumeric.io">eric@alphanumeric.io</a>
    </p>
  </section>
</template>

<style scoped>
  .thanks {
    margin-top: 2rem;
  }
  
  .thanks__txt {
    font-size: 1.4rem;
    font-weight: 400;
    grid-column: 2 / span 10;
  }

  .italic {
    font-style: italic;
  }

  a {
    color: #0C26B0;
  }

  @media (min-width: 900px) {

    .thanks {
      margin-top: 8rem;
    }

    .thanks__txt {
      font-size: 3.125rem;
    }
  }
</style>