<template>
  <!--  <li>
    <strong>Artikel: </strong> {{ productItem.artikelName }},
    <strong>Preis:</strong> {{ productItem.price }}€
  </li> -->
  <li :class="{ 'notAvailable' : !carsItem.available }" class="li-back">
    <strong>Model: </strong> {{ carsItem.model }}, <strong>brand:</strong>
    {{ carsItem.brand }}
    <!-- TWO WAY DATA BINDING -->
    <!-- custom event -->
    <button @click="toggleTest()">Toggle</button>
  </li>
</template>

<script>
export default {
  name: "ShopArtikelItem",
  //props im html kebab-case
  //im js camelCase
  props: ["productItem", "carsItem"],
  methods: {
    toggleTest() {
      // custom events
     this.$emit('customToggle', this.carsItem )
    }
  }
};
</script>

<style scoped>
.li-back {
  background: yellow;
  width: fit-content; 
  color: black;
}
</style>
