<template>
  <v-app>
    <Navbar />
    <Cards />
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar";
import Cards from "./components/Cards";

export default {
  name: "App",

  components: {
    Navbar,
    Cards
  },

  data: () => ({
    //
  })
};
</script>
