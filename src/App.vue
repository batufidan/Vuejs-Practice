<template>
  <v-app>
    <Header />
    <v-main>
      <HeroComponent />
      <Aboutus />
      <Product /> 
      <Gallery />
      <Contact />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Header from "@/components/Header";
import HeroComponent from "./components/HeroComponent.vue";
import Aboutus from "./components/Aboutus.vue";
import Product from "./components/Product.vue";
import Gallery from "./components/Gallery.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";

export default {
  name: 'App',
  components: {
    Header,
    HeroComponent,
    Aboutus,
    Product,
    Gallery,
    Contact,
    Footer
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
