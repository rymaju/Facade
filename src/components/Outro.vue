<template>
  <div class="intro">
    <b-container class="content">
      <div>
        <div class="fade-1">
          <h1>Recap</h1>

          <ul>
            <li>Cookies aren't inherently evil, just a tool often used to track you as you move online.</li>
            <li>
              Recomendation systems track your actions, and use them to label you as a member of a group (age, race, gender, likes, and dislikes).
              While uncomfortable, usually this a feature that you can disable and that you benefit from.
            </li>
            <li>
              Some websites collect, buy, and sell Personally Indentifiable Information that you provide through forms,
              login information, or access to other apps. Personal information is often sold to Data Brokers,
              who can use your private information for whatever they want. This is extremely morally questionable.
            </li>
          </ul>
          <h2>What can we do?</h2>
          <p>As the average consumer, basically nothing other than to be careful about sharing personal information like phone numbers or access to friends or contacts. As it stands, this kind of data collection is legal and incentivized. The best we can do is be aware and advocate for change.</p>
          <h3>How can I learn about what Big Data knows about me?</h3>
          <ul>
            <li>
              <a href="https://adssettings.google.com/" target="_blank">What Google knows about you</a>
            </li>
            <li>
              <a
                href="https://twitter.com/settings/your_twitter_data/ads"
                target="_blank"
              >What Twitter knows about you</a>
            </li>
            <li>
              <a
                href="https://www.facebook.com/help/212802592074644"
                target="_blank"
              >What Facebook knows about you</a>
            </li>
          </ul>
          <h3>More information</h3>
          <ul>
            <li>
              <a
                href="https://www.youtube.com/watch?v=HFyaW50GFOs"
                target="_blank"
              >Vox: How cookies track you</a>
            </li>
            <li>
              <a
                href="https://mislove.org/publications/PII-PETS.pdf"
                target="_blank"
              >Northeastern's Professor Mislove: How Facebook harvests your PII for targeted ads</a>
            </li>
          </ul>
        </div>
        <b-button class="fade-2" size="md" squared variant="outline-light">
          <p class="lead m-0" @click="() => {this.$emit('continue')}">Back to the Beginning</p>
        </b-button>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Outro",
  data() {
    return {};
  },
  methods: {}
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

@keyframes fade {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
