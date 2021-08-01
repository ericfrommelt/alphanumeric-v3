<template>
  <div class="marquee">
    <div class="marquee-wrap">
      <ul>
        <li class="c1">Design Technologist</li>
        <li class="c2">UX Engineer</li>
        <li class="c3">Design Engineer</li>
        <li class="c4">UI Developer</li>
        <li class="c1">Front End Developer</li>
        <li class="c2">Creative Engineer</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
  .c1 {
    color: #FF0005;
  }

  .c2 {
    color: #546ADC;
  }

  .c3 {
    color: #54E6EF;
  }

  .c4 {
    color: #EF54CD;
  }

  .marquee {
    position: relative;
    width: 100%;
  }

  .marquee-wrap {
    display: block;
    width: max-content;
  }

  ul {
    list-style: none;
    display: flex;
    animation: move 40s linear infinite;
  }

  li {
    font-weight: 200;
    font-size: 3rem;
    font-style: italic;
    white-space: nowrap;
    padding: 0 1rem;
  }

  @media (min-width: 900px) {
    li {
      font-size: 7rem;
    }
  }

  @keyframes move {
    0% { transform: translateX(calc(100vw)); }
    100% { transform: translateX(-100%); }
  }

</style>