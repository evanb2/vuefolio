<template>
  <div class="slide__background" @click="store.setSlideNum('SlideTwo')">
    <h1 class="slide__title">
      Web Architect
    </h1>
  </div>
</template>

<style lang="scss">
  .slide__title {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
  }

  .slide__background {
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url('../assets/img/slide-one-bg.jpg');
  }

  .slide__background:hover {
    cursor: pointer;
  }
</style>

<script>
  export default {
    props: {
      store: Object,
    },
  };
</script>
