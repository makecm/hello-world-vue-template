<template>
  <div class="logos">
    <img src="../assets/logo.svg" />
    <div class="seperator" />
    <img src="../assets/vue-logo.svg" />
  </div>
</template>

<script>
  export default {
    name: 'Logos',
  }
</script>

<style scoped>
  .logos {
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: 1fr 0.25fr 1fr;
    place-items: center;
    background-color: #1f2a44;
    padding: clamp( 0.5rem, 5vw, 2rem);
    border-radius: 3rem;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.15);
  }

  .logos img {
    display: block;
    width: clamp( 1rem, 5vw, 3rem);
    height: clamp( 1rem, 5vw, 3rem);
  }

  .seperator {
    place-self: flex-end;
    border-left: 2px solid white;
    height: 100%;
  }
</style>
