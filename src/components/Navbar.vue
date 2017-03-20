<template>
  <nav class="nav has-shadow">
    <div class="container">
      <div class="nav-left">
        <a class="nav-item">
          <img src="http://bulma.io/images/bulma-logo.png" alt="Bulma logo">
        </a>
        <a class="nav-item is-tab is-hidden-mobile"
           :class="[store.slideNum === 'SlideOne' ? 'is-active' : '']"
           @click="store.setSlideNum('SlideOne')">
          About
        </a>
        <a class="nav-item is-tab is-hidden-mobile"
           :class="[store.slideNum === 'SlideTwo' ? 'is-active' : '']"
           @click="store.setSlideNum('SlideTwo')">
          CV
        </a>
        <a class="nav-item is-tab is-hidden-mobile"
           :class="[store.slideNum === 'SlideThree' ? 'is-active' : '']"
           @click="store.setSlideNum('SlideThree')">
          Adventures/Projects
        </a>
      </div>
      <span class="nav-toggle">
        <span></span>
        <span></span>
        <span></span>
      </span>
      <div class="nav-right nav-menu">
        <a class="nav-item is-tab is-hidden-tablet is-active">About</a>
        <a class="nav-item is-tab is-hidden-tablet">CV</a>
        <a class="nav-item is-tab is-hidden-tablet">Adventures/Projects</a>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    props: {
      store: Object,
    },
  };
</script>
