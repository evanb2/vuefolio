<template>
  <div class="slide__background" @click="store.setSlideNum('SlideOne')">
    <h1 class="slide__title">
      Contact
    </h1>
  </div>
</template>

<script>
  export default {
    props: {
      store: Object,
    },
  };
</script>