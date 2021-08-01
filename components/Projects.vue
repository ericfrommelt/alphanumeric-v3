<template>
  <section class="grid__wrapper projects">
    <div class="section__block"></div>
    <h2>Projects—</h2>
    <!-- 01 Terminal Index -->
    <span class="project__number">01</span>
    <div class="project__details">
      <h3 class="project__title">Terminal Index</h3>
      <h4 class="project__subhead">Interaction sketchbook</h4>
      <p class="project__role">Design + Development</p>
      <p class="project__description">I wanted to build a space where I could post small, isolated interaction design experiments on an ongoing basis.</p>
      <div class="project__button">
        <a href="https://www.terminalindex.net/">Go to site</a>
      </div>
      <div class="tools">
        <div class="subsection__block"></div>
        <h5>Tools + technogy</h5>
        <ul class="tools__list">
          <li>Vue</li>
          <li>Nuxt</li>
          <li>CSS</li>
          <li>GSAP</li>
        </ul>
      </div>
    </div>
    <div class="project__video">
      <video src="TerminalIndex.mp4" loop muted autoplay></video>
    </div>
    <div class="project__footer"></div>

    <!-- 02 HPE -->
    <span class="project__number">02</span>
    <div class="project__details">
      <h3 class="project__title">HPE</h3>
      <h4 class="project__subhead">Editorial Experiences</h4>
      <p class="project__role">Design + Development</p>
      <p class="project__description">Editorial experience design and development for HPE.</p>
      <div class="project__button">
        <a href="https://blissful-lichterman-3559c0.netlify.app/">Go to site</a>
      </div>
      <div class="tools">
        <div class="subsection__block"></div>
        <h5>Tools + technogy</h5>
        <ul class="tools__list">
          <li>React</li>
          <li>Gatsby</li>
          <li>CSS Modules</li>
          <li>GSAP</li>
          <li>D3</li>
        </ul>
      </div>
    </div>
    <div class="project__video">
      <video src="hpe.mp4" loop muted autoplay></video>
    </div>
    <div class="project__footer"></div>

    <!-- 03 Vaporized Claims -->
    <span class="project__number">03</span>
    <div class="project__details">
      <h3 class="project__title">Vaporized Claims</h3>
      <h4 class="project__subhead">CSS Art</h4>
      <p class="project__role">Design + Development</p>
      <p class="project__description">I've been enamored with collage since childhood and saw an opportunity to experiment with the process utiliziing CSS grid, clip-path and simple animation. So much fun.</p>
      <div class="project__button">
        <a href="#">View project</a>
      </div>
      <div class="tools">
        <div class="subsection__block"></div>
        <h5>Tools + technogy</h5>
        <ul class="tools__list">
          <li>HTML</li>
          <li>CSS</li>
        </ul>
      </div>
    </div>
    <div class="project__video">
      <video src="VaporizedClaims.mp4" loop muted autoplay></video>
    </div>
    <div class="project__footer"></div>
  </section>
</template>

<style scoped>
  h2 {
    font-style: italic;
    font-size: 1.4rem;
    font-weight: 400;
    grid-column: 2 / span 10;
  }

  h3 {
    margin-top: 0;
    margin-bottom: .4rem;
    font-size: 1.8rem;
  }

  h4 {
    margin: 0;
  }

  ul {
    list-style: none;
    padding: 0;
    display: flex;
  }

  .projects {
    margin-top: 6rem;
  }

  .project__details {
    grid-column: 2 / span 10;
  }

  .project__image, .project__video {
    grid-column: 2 / span 10;
    margin: 2rem 0;
  }

  .project__footer {
    grid-column: 2 / span 10;
    padding-bottom: 8rem;
  }

  .project__number {
    grid-column: 2 / span 10;
    font-family: ibm-plex-sans-condensed;
    font-size: 1rem;
    font-weight: 200;
    padding-right: 1rem;
    color: hsl(0, 0%, 70%);
  }

  .project__role {
    color: hsl(0, 0%, 70%);
  }

  .project__subhead {
    font-weight: 400;
    font-size: 1.2rem;
  }

  .tools__list li {
    padding-right: 1rem;
  }

  @media (min-width: 900px) {
    h2 {
      font-size: 3.125rem;
    }

    .project__details {
      grid-column: 2 / span 5;
    }

    .project__image, .project__video {
      grid-column: 7 / span 5;
    }

    .project__number {
      grid-column: 1;
      justify-self: end;
      font-size: 1.8rem;
    }
  }
</style>