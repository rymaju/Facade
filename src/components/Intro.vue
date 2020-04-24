<template>
  <div class="intro">
    <b-container class="content">
      <div class="intro-fade" v-if="showTitleScreen">
        <h1 class>How websites track you</h1>
        <p
          class="lead"
        >An explorable explanation of tactics used to track and label you on the internet.</p>
        <p class="about">Made for ARTF 2223, by Ryan Jung</p>

        <b-button class size="md" squared variant="outline-light" @click="nextSlide">
          <p class="leaf m-0">Next</p>
        </b-button>
      </div>

      <div v-else>
        <p class="lead fade-1">Websites are used to entertain, promote, inform...</p>

        <p class="lead fade-2">and track its users.</p>

        <p class="lead fade-3">
          A startling amount of websites are collecting
          <b>Personally Identifiable Information</b>
          on you, to target and label you for commerical and political gain.
        </p>

        <p class="lead fade-4">
          The following is a fake website, meant to shed light on the tactics used by
          <b>real</b>
          websites to collect your information.
        </p>
        <b-button class="fade-5" size="md" squared variant="outline-light">
          <p class="lead m-0" @click="() => {this.$emit('continue')}">Next</p>
        </b-button>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Intro",
  data() {
    return {
      showTitleScreen: true
    };
  },
  methods: {
    nextSlide() {
      this.showTitleScreen = false;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.intro {
  background: black;
  width: 100%;
  height: 100%;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.content {
  color: whitesmoke;
  width: 50em;
  max-width: 100%;
}
.about {
  margin-bottom: 2em;
}

.intro-fade {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-fill-mode: both;
}

.fade-1 {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-delay: 0.5s;
  animation-fill-mode: both;
}
.fade-2 {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-delay: 2s;
  animation-fill-mode: both;
}

.fade-3 {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-delay: 4s;
  animation-fill-mode: both;
}

.fade-4 {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-delay: 7s;
  animation-fill-mode: both;
}
.fade-5 {
  opacity: 0;
  animation-name: fade;
  animation-duration: 2s;
  animation-delay: 9s;
  animation-fill-mode: both;
}

@keyframes fade {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
