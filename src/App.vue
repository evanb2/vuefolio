<template>
  <div>
    <navbar :store="store"></navbar>
    <!--<component :is="store.slideNum" :store="store"></component>-->
  </div>
</template>

<style lang="scss">

</style>

<script>
  import Vue from 'vue';
  import Navbar from './components/Navbar';
  import SlideOne from './components/SlideOne';
  import SlideTwo from './components/SlideTwo';

  export default {
    components: {
      Navbar,
      SlideOne,
      SlideTwo,
    },
    /**
     * Slides:
     *  "Web Architect"
     *  Adventure/Challenge
     *  "Tools" i.e. skills
     *  Contact page
     */
    data() {
      return {
        store: {
          slideNum: 'SlideOne',
          setSlideNum(slide) {
            Vue.set(this, 'slideNum', slide);
          },
        },
      };
    },
  };
</script>
