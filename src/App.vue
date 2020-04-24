<template>
  <div id="app">
    <transition name="fade">
      <Intro v-if="slideNumber == 1" v-on:continue="slideNumber = 2" />
      <SiteHome v-else-if="slideNumber == 2" v-on:continue="slideNumber = 3" />
      <Outro v-else v-on:continue="slideNumber = 1" />
    </transition>
  </div>
</template>

<script>
import Intro from "./components/Intro.vue";
import SiteHome from "./components/SiteHome.vue";
import Outro from "./components/Outro.vue";
export default {
  name: "App",
  components: {
    Intro,
    SiteHome,
    Outro
  },
  data() {
    return {
      slideNumber: 3
    };
  }
};
</script>

<style>
#app {
  width: 100%;
  height: 100%;
  min-height: 100vh;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
