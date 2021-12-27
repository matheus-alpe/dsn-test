<template>
  <div id="app">
    <Header />

    <main>
      <Filters />

      <Products />

      <Newsletter />

      <About />
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from "./Header.vue";
import Filters from "./Filters.vue";
import Products from "./Products.vue";
import Newsletter from "./Newsletter.vue";
import About from "./About.vue";
import Footer from "./Footer.vue";

export default {
  name: "LandingPage",
  components: {
    Header,
    Filters,
    Products,
    Newsletter,
    About,
    Footer,
  },
};
</script>