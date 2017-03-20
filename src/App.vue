<template>
  <div>
    <navbar :store="store"></navbar>
    <div class="app__background">
      <!--<component :is="store.slideNum" :store="store"></component>-->
    </div>
  </div>
</template>

<style lang="scss">
  .app__background {
    /*background-size: 100% 100%;*/
    height: 770px;
    background: url('./assets/img/center_ridge.jpg') no-repeat;
  }
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
