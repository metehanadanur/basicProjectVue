<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <button>Main Button</button>
  <HelloWorld :msg="name" />
  <HelloWorld msg="Zweite Komponente"></HelloWorld>
  <GetGreeting :name-props="teacherName"></GetGreeting>
  <GetGreeting :name-props="teacherName" :member-list="fullstackgroup" />
  <ShopArtikel />
  <ShopArtikel />
  <!-- <div class="artikel">
    Test Artikel
  </div> -->
  <hr />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import GetGreeting from "./components/GetGreeting.vue";
import ShopArtikel from "./components/ShopArtikel.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    GetGreeting,
    ShopArtikel,
  },
  data() {
    return {
      name: "Basri Konuskan",
      teacherName: "Metehan",
      fullstackgroup: [
        "Ulga",
        "Al-Enasy",
        "Konuskan",
        "Ertosun",
        "Sakalli",
        "Kök",
        "Adanur",
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
