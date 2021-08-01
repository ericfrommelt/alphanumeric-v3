<template>
  <div ref="introRef" class="intro-wrapper">
    <div id="black-wipe"></div>
    <div id="white-wipe"></div>
    <div class="content-wrapper">
      <h1 id="name">Eric Frommelt</h1>
      <h2 id="job-title">Design Technologist</h2>
      <h1 ref="titleRef" id="alpha">{{ title }}</h1>
      <div id="big-char">3</div>
      <div id="big-char-2">X</div>
      <div id="big-char-3">2</div>
    </div>
  </div>
</template>

<style scoped>
  .intro-wrapper {
    background-color: white;
    height: 100vh;
    overflow: hidden;
  }

  .content-wrapper {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto 80vh auto;
    height: 100vh;
    align-items: center;
  }

  h1 {
    font-size: 1.4rem;
    font-family: ibm-plex-sans, sans-serif;
    font-style: normal;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1.8rem;
  }
  
  #alpha, #big-char, #big-char-2, #job-title, #name {
    grid-row: 2;
  }

  #alpha {
    grid-column: 1 / span 12;
    justify-self: center;
    color: var(--primary-color-dark)
  }

  #big-char, #big-char-2, #big-char-3 {
    font-family: "Didot 64 A", "Didot 64 B";
    font-style: normal;
    font-weight: 300;
    text-transform: uppercase;
    color: black;
  }

  #big-char {
    grid-column: 8 / span 4;
    justify-self: center;
    font-size: 36rem;
    margin-top: -20rem;
  }

  #big-char-2 {
    grid-column: 1 / span 4;
    font-size: 20rem;
    align-self: end;
    margin-left: -4rem;
  }

  #big-char-3 {
    grid-column: 1 / span 12;
    position: absolute;
    top: -50rem;
    left: 20rem;
    font-size: 60rem;
  }

  #black-wipe {
    position: absolute;
    background-color: var(--primary-color-dark);
    height: 100%;
    width: 100%;
  }

  #white-wipe {
    position: absolute;
    background-color: var(--primary-color-light);
    height: 100%;
    width: 100%;
  }

  #job-title {
    grid-column: 1 / span 12;
    justify-self: center;
    font-family: "Mercury SSm A", "Mercury SSm B";
    font-style: normal;
    font-weight: 400;
    font-size: 1.2rem;
    color: var(--primary-color-light);
    text-transform: uppercase;
    letter-spacing: 1rem;
    padding-top: 8rem;
    margin-left: -.4rem;
  }

  #name {
    grid-column: 1 / span 12;
    font-size: 2.4rem;
    justify-self: center;
    color: var(--primary-color-light);
    z-index: 1000;
  }
</style>

<script>
  export default {
    mounted() {
      this.introAnimation()
    },

    data() {
      return {
        title: 'alphanumeric'
      }
    },

    methods: {

      // changeTitle() {
      //   console.log(this.$refs.titleRef.firstChild.childNodes)
      //   this.$refs.titleRef.remove()
      // },

      removeIntro() {
        console.log('remove intro fired')
        this.$refs.introRef.remove()
        this.$emit('removeIntro')
      },

      introAnimation() {

        const master = this.$gsap.timeline()
        const tl = this.$gsap.timeline()
        const tl2 = this.$gsap.timeline()

        const SplitText = this.$SplitText
        const CustomEase = this.$CustomEase

        const alphaSplit = new SplitText("#alpha", { type: "words, chars", charsClass: "alpha++" })
        const nameSplit = new SplitText("#name", { type: "chars" })
        const jobTitleSplit = new SplitText("#job-title", { type: "chars" })

        const alp = alphaSplit.chars.slice(0, 3)
        const ha = alphaSplit.chars.slice(3, 5)
        const num = alphaSplit.chars.slice(5, 8)
        const e = alphaSplit.chars.slice(8, 9)
        const ric = alphaSplit.chars.slice(9, 12)
        const eric = alphaSplit.chars.slice(8, 12)
        const textN = alphaSplit.chars.slice(5, 6)
        const textU = alphaSplit.chars.slice(6,7)
        const frommelt = alphaSplit.chars.slice(12, 20)
        const ericfrommelt = nameSplit.chars.slice(0, 12)
        const jobTitle = jobTitleSplit.chars.slice()

        console.log(nameSplit.chars[0])

        this.$gsap.set("#black-wipe", { height: 0 })
        this.$gsap.set("#white-wipe", { height: 0 })
        this.$gsap.set(alp, { opacity: 0 })
        this.$gsap.set(ha, { opacity: 0, y: +100 })
        this.$gsap.set(num, { opacity: 0, y: +200 })
        this.$gsap.set(e, { opacity: 0, y: +400 })
        this.$gsap.set(ric, { opacity: 0, y: +300 })
        this.$gsap.set("#big-char", { opacity: 0 })
        this.$gsap.set("#big-char-2", { opacity: 0 })
        this.$gsap.set("#big-char-3", { opacity: 0 })
        this.$gsap.set(ericfrommelt, { opacity: 0, x: +200, rotateY: +90 })

        // this.$gsap.set(nameSplit.chars, { rotateY: +180})
        this.$gsap.set(jobTitle, { opacity: 0, rotateY: +90 })

        CustomEase.create("alphaEase", "M0,0 C0.022,0.566 0.446,1 1,1")
        CustomEase.create("wipe", "M0,0 C0.11,0.494 0.374,0.374 0.5,0.5 0.632,0.632 0.504,1 1,1")
        CustomEase.create("nameIn", "M0,0 C0.558,0.02 -0.034,1 1,1 ")

        
        // Scene 1
        tl.to(alp, { duration: 0.2, opacity: 1, y: 0, stagger: 0.1 })
        tl.to(ha, { duration: 0.2, opacity: 1, y: 100, stagger: 0.1 })
        tl.to(num, { duration: 0.2, opacity: 1, y: 200, stagger: 0.1 })
        tl.to(textN, { duration: 0.2 })
        tl.to(textU, { duration: 0.2 })
        tl.to(ric, { duration: 0.2, opacity: 1, y: 300, stagger: 0.1 })
        tl.to(e, { duration: 0.2, opacity: 1 })
        tl.to(e, { duration: 0.6, opacity: 1, y: 300, stagger: 0, ease: "alphaEase" })

        tl.to("#big-char-3", { duration: 2, opacity: 0.1 }, "-=2")
        tl.to("#big-char-2", { duration: 2, opacity: 0.1 }, "-=1")
        tl.to("#big-char", { duration: 2, opacity: 0.1 }, "-=.5")

        tl.to(alp, { duration: 0.2, opacity: 0, y: 0, stagger: 0.1 })
        tl.to(ha, { duration: 0.2, opacity: 0, y: 100, stagger: 0.1 })
        tl.to(num, { duration: 0.2, opacity: 0, y: 200, stagger: 0.1 })
        tl.to(eric, { duration: 0.2, opacity: 0, stagger: 0.1 })

        // tl.eventCallback("onComplete", changeTitle)

        tl.to("#black-wipe", { duration: 1.6, height: "100vh", ease: "wipe" })
        tl.to("#big-char-3", { duration: 2, opacity: 0 }, "-=2")
        tl.to("#big-char-2", { duration: 2, opacity: 0 }, "=-1.5")
        tl.to("#big-char", { duration: 2, opacity: 0 }, "-=1")

        // Scene 2
        tl2.eventCallback("onComplete", this.removeIntro)
        tl2.to(ericfrommelt, { duration: 2, opacity: 1, x: 0, stagger: 0.1, ease: "nameIn", rotateY: 0 })
        tl2.to(jobTitle, { duration: 2, opacity: .9, x: 0, stagger: 0.1, ease: "nameIn", rotateY: 0 }, "-=2")
        tl2.to("#white-wipe", { duration: 1.6, height: "100vh", ease: "wipe" })
          


        master.add(tl)
        master.add(tl2)

        function removeTl() {
          console.log('remove fired')
          master.remove(tl)
        }
      }
    }
  }
</script>