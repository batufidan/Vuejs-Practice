<template>
  <v-app>
    <Header />
    <v-main>
      <HeroComponent />
      <Aboutus />
      <Portfolio />
      <Product /> 
    </v-main>
  </v-app>
</template>

<script>
import Header from "@/components/Header";
import HeroComponent from "./components/HeroComponent.vue";
import Aboutus from "./components/Aboutus.vue";
import Portfolio from "./components/Portfolio.vue";
import Product from "./components/Product.vue";

export default {
  name: 'App',
  components: {
    Header,
    HeroComponent,
    Aboutus,
    Portfolio,
    Product,
},

  data(){
    return {
      menus: [
        {title: 'Home', route: 'home'},
        {title: 'About Us', route: 'about-us'},
        {title: 'Portfolio', route: 'portfolio'},
        {title: 'Project', route: 'project'},
        {title: 'Gallery', route: 'gallery'},
        {title: 'Contact', route: 'contact'},

      ]
    }
  },
};
</script>
