<template>
  <div id="app" v-bind:style="{ backgroundImage: 'url(' + makeTemplateProps.backgroundImage + ')' }">

    <div v-if="makeTemplateProps.showLogos" style="z-index: 2;">
      <Logos />
    </div>

    <h1>{{ makeTemplateProps.headline }}</h1>

    <Shapes />

  </div>
</template>

<script>
import Logos from './components/Logos.vue';
import Shapes from './components/Shapes.vue';

const makeTemplateMixin = {
  computed: {
    makeTemplateProps() {
      return window.templateProps || {
        headline: "Hello World",
        showLogos: true,
        backgroundImage: '',
      };
    }
  }
}

export default {
  name: 'App',
  components: {
    Logos,
    Shapes
  },
  mixins: [makeTemplateMixin]
}
</script>

<style>
  body {
    margin: 0;
    font-family: 'IBM Plex Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
      sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  #app {
    width: 100vw;
    height: 100vh;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    text-align: center;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  h1 {
    font-size: clamp( 16px, 10vh, 250px);
    font-weight: 700;
    line-height: 100%;
    color: #1f2a44;
    text-align: center;
    width: 100%;
    padding: 0 2rem;
    z-index: 1;
  }
</style>
