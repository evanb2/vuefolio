<template>
  <section class="hero is-fullheight">
    <!-- Hero header: will stick at the top -->
    <div class="hero-head">
      <header class="nav">
        <div class="container">
          <div class="nav-left">
            <a class="nav-item">
              <!--<img src="images/bulma-type-white.png" alt="Logo">-->
            </a>
          </div>
          <span class="nav-toggle">
          <span></span>
          <span></span>
          <span></span>
        </span>
          <div class="nav-right nav-menu">
            <a class="nav-item is-active">
              Home
            </a>
            <a class="nav-item">
              Examples
            </a>
            <a class="nav-item">
              Documentation
            </a>
            <span class="nav-item">
            <a class="button is-success is-inverted">
              <span class="icon">
                <i class="fa fa-github"></i>
              </span>
              <span>Download</span>
            </a>
          </span>
          </div>
        </div>
      </header>
    </div>
    <!-- Hero content: will be in the middle -->
    <div class="hero-body wallpaper">
      <div class="container has-text-centered">
        <h1 class="title">
          Evan Butler
        </h1>
        <h2 class="subtitle">
          Full Stack Developer
        </h2>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
  .wallpaper {
    background-size: cover;
    /*margin-top: 10%;*/
    /*height: 770px;*/
    background: url('./assets/img/jefferson_pano.jpg') no-repeat fixed;
  }
</style>

<script>
  import Vue from 'vue';
  import Navbar from './components/Navbar';
  import Home from './components/Home';
  import Resume from './components/Resume';
  import Adventures from './components/Adventures';

  export default {
    components: {
      Home,
      Navbar,
      Resume,
      Adventures,
    },
    data() {
      return {
        store: {
          slideNum: 'Home',
          setSlideNum(slide) {
            Vue.set(this, 'slideNum', slide);
          },
        },
      };
    },
  };
</script>
