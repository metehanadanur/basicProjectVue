<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="test">Click me</button>
    <ul>
      <li v-for="car in cars" :key="car">{{ car }}</li>
    </ul>
  </div>
  <!-- <GetGreeting></GetGreeting> -->
</template>

<script>
//import GetGreeting from "./GetGreeting.vue";

export default {
  name: "HelloWorld",
  components: {
    // GetGreeting,
  },
  props: {
    msg: String,
  },
  methods: {
    test() {
      alert("Funktioniert");
    },
  },
  data() {
    return {
      cars: ["BMW", "Porsche", "Mercedes", "Audi"],
    };
  },
  computed: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

button {
  padding: 1rem 3rem;
  background: red;
  color: white;
}
</style>
