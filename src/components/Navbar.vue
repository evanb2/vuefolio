<template>
  <nav class="nav has-shadow">
    <div class="container">
      <div class="nav-left">
        <a class="nav-item" @click="store.setSlideNum('Home')">
          <img src="http://bulma.io/images/bulma-logo.png" alt="Bulma logo">
        </a>
        <a class="nav-item is-tab is-hidden-mobile"
           :class="[store.slideNum === 'Resume' ? 'is-active' : '']"
           @click="store.setSlideNum('Resume')">
          CV
        </a>
        <a class="nav-item is-tab is-hidden-mobile"
           :class="[store.slideNum === 'Adventures' ? 'is-active' : '']"
           @click="store.setSlideNum('Adventures')">
          Adventures/Projects
        </a>
      </div>
      <span class="nav-toggle">
        <span></span>
        <span></span>
        <span></span>
      </span>
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
