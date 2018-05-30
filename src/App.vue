<template>
  <div id="main">
    <div id="app">
      <img src="./assets/image/logo.png">
    <VuePerfectScrollbar id="scroll-container" v-once :settings="settings" @ps-scroll-y="scrollHanle">
      
      <HelloWorld msg="Hi, Mashiro!" />
      <LinkItems />
    </VuePerfectScrollbar>
    </div>
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue';
  import LinkItems from './components/LinkItems.vue';
  import VuePerfectScrollbar from 'vue-perfect-scrollbar';

  export default {
    name: 'app', // Just a name...?
    components: {
      HelloWorld,
      LinkItems,
      VuePerfectScrollbar
    },
    data() {
      return {
        settings: {
          wheelSpeed: 0.5,
          wheelPropagation: true,
          minScrollbarLength: 5
        }
      }
    }
  }
</script>

<style>
  html {
    padding: 0;
    margin: 0;
    height: 100%;
    width: 100%;
    overflow: hidden;
  }

  body {
    background-image: url(./assets/image/bg.png);
    background-repeat: no-repeat;
    background-size: cover;
    position: absolute;
    width: 100%;
    height: 100%;
    margin: 0;
  }

  #main {
    margin: 5%;
    height: 80%;
  }

  #app {
    font-family: 'Comic Sans', cursive;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color: rgba(255, 255, 255, 0.7);
    width: auto;
    max-width: 800px;
    margin: auto;
    display: block;
    height: 100%;
    overflow: hidden;
    border-radius: 10px
  }

  #app img {
    margin-top: 20px;
  }

  #app #scroll-container {
    width: 100%;
    height: 85%;
  }
</style>