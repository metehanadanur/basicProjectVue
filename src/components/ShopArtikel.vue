<template>
  <div class="artikel">
    <!--     <ul>
      <ShopArtikelItem
        v-for="artikel in artikelListe"
        :key="artikel.id"
        :product-item="artikel"
      />
    </ul> -->
    <ul>
      <ShopArtikelItem
        v-for="cars in carsList"
        :key="cars.id"
        :cars-item="cars"
        @customToggle="changeAvailable"
      />
    </ul>
  </div>
</template>

<script>
import ShopArtikelItem from "./ShopArtikelItem.vue";

export default {
  name: "ShopArtikel",
  data() {
    return {
      // artikelListe: [
      //   { id: 1, price: 49.99, artikelName: "Hoodie" },
      //   { id: 2, price: 69.99, artikelName: "Jacke" },
      //   { id: 3, price: 199.99, artikelName: "Schuhe" },
      //   { id: 4, price: 24.99, artikelName: "T-Shirt" },
      // ],
      carsList: [
        {
          id: 1,
          model: "C-Klasse",
          brand: "Mercedes",
          available: true,
        },
        {
          id: 2,
          model: "335i",
          brand: "BMW",
          available: false,
        },
        {
          id: 3,
          model: "SQ8",
          brand: "Audi",
          available: true,
        },
      ],
    };
  },
  methods: {
    changeAvailable(currentCar) {
      console.log(currentCar);
      currentCar.available = !currentCar.available;
    },
  },
  components: {
    ShopArtikelItem,
  },
};
</script>

<style>
.artikel {
  padding: 2rem;
  border: 3px dashed black;
  background: green;
  color: white;
}
ul {
  list-style-type: none;
}
li {
  margin-bottom: 1rem;
  text-align: left;
}

.notAvailable {
  text-decoration: line-through;
  color: red !important;
}
</style>
