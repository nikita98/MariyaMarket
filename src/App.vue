<template>
  <div id="app">

    <SnowBackground />
    <HeaderMain />
    <HeroSection />
    <AuI />
  </div>
</template>

<script>
import SnowBackground from './components/SnowBackground.vue'
import HeaderMain from './components/HeaderMain.vue'
import AuI from './components/AuI.vue';
import HeroSection from './components/HeroSection.vue';

export default {
  name: 'App',
  components: {
    SnowBackground, HeaderMain, AuI, HeroSection
  }
}
</script>

<style type="scss">
/* 
@font-face {
  font-family: "Lobster";
  src: local("Lobster"), url(./fonts/Lobster-Regular.ttf);
} */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --primary-red: #E03C3C;
  --primary-dark: #C42D2D;
  --accent-red-light: #FF6B6B;
  --bg-cream: #FDF8F3;
  --bg-warm: #FAF3EB;
  --text-dark: #2C2C2C;
  --text-light: #5A5A5A;
  --white: #FFFFFF;
  --shadow-soft: 0 4px 20px rgba(224, 60, 60, 0.1);
  --shadow-medium: 0 8px 30px rgba(224, 60, 60, 0.15);
  --border-radius: 16px;
  --border-radius-large: 24px;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: var(--bg-cream);
  color: var(--text-dark);
  line-height: 1.7;
  font-size: 16px;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  min-height: 100vh;
  background-color: #c52e2e;

  .button {
    display: flex;
    font-size: 16px;
    background: var(--primary-red);
    color: var(--white);
    padding: 12px 24px;
    border-radius: 30px;
    text-decoration: none;
    font-size: 0.9rem;
    margin-bottom: 25px;
    animation: pulse 2s infinite;
    font-weight: 500;
    transition: all 0.3s ease;
  }


  .button:hover {
    background: var(--primary-dark);
    transform: translateY(-2px);
    box-shadow: 0 4px 15px rgba(224, 60, 60, 0.4);
  }
}



h1,
h2,
h3,
h4,
.handwritten {
  font-family: 'Caveat', cursive;
  font-weight: 500;
}

h2 {
  font-size: 2.8rem;
  margin-bottom: 1rem;
  color: var(--text-dark);
}

h3 {
  font-size: 1.8rem;
  margin-bottom: 0.8rem;
}

p {
  margin-bottom: 1rem;
  color: var(--text-light);
}


/* box model */
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* base */
html {
  line-height: 1.15;
  -webkit-text-size-adjust: 100%;
}

body {
  margin: 0;
}

/* typography */
h1,
h2,
h3,
h4,
h5,
h6,
p,
figure,
blockquote {
  margin: 0;
}

/* media */
img,
video,
canvas,
svg {
  display: block;
  max-width: 100%;
}

/* forms */
button,
input,
textarea,
select {
  font: inherit;
}

/* links */
a {
  color: inherit;
  text-decoration: none;
}

/* lists */
ul,
ol {
  margin: 0;
  padding: 0;
  list-style: none;
}
</style>
