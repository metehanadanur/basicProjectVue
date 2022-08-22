<template>
  <div class="greeting">
    <h1>Hallo {{ name }}</h1>
    <h1>Teacher: {{ nameProps }}</h1>
    <ul>
      <li v-for="member in memberList" :key="member">{{ member }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "GetGreeting",
  data() {
    return {
      name: "Mehmet Ulga",
      schueler: ["Max Mustermann", "Luise Meyer", "Thomas Tuchel"],
    };
  },
  // props: ["nameProps", "memberList", "isFinished" , "numberOfAccomplishments"],
  props: {
    nameProps: {
      type: String,
      required: true,
      default: "Fullstack Lehrer fehlt",
    },
    memberList: {
      type: Array,
      //type: Object,
      required: false,
      default() {
        return ["Hallo", "Merhaba", "Selam", "Ciao"];
        //return { name: "cool" };
      },
    },
    isFinished: Boolean,
    numberOfAccomplishments: Number,
  },
  methods: {},
};
</script>

<style scoped>
.greeting {
  padding: 2rem;
  border: 2px dashed black;
  background-color: rebeccapurple;
  color: white;
  margin: 1rem;
}
</style>
