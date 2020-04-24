<template>
  <b-card :img-src="img" img-alt="phone case image" img-top class="card" border-variant="light">
    <p class="lead card-title">{{this.title}}</p>
    <b-card-text>{{this.price}}</b-card-text>
  </b-card>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
    price: String,
    img: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  width: 14em;
  margin: auto;
  margin-bottom: 2em;
  cursor: pointer;
  transition: transform 0.1s;
  box-shadow: 1px 1px 4px 0px grey;
}
.card:hover {
  transform: scale(1.025);
}
.card-title {
  margin: 0;
  font-size: 1.2em;
}
</style>
