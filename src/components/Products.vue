<template>
  <section class="products">
    <Card v-for="product in products" :key="product.id" :product="product" />
  </section>
</template>

<script>
import Card from "@/components/Card.vue";

export default {
  ame: "Products",
  components: {
    Card,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Notebook Linx Impulse Premium 8GB RAM SSD 500GB Tela 15,6 Windows 10",
          image_url: "https://i.imgur.com/zu9NkxS.png",
          brand: "Linx",
          oldPrice: 4199.9,
          price: 3569.9,
          available: true,
          details: {
            freeShipping: true,
          },
        },
        {
          id: 2,
          name: "Smartphone Linx 6 GB RAM",
          image_url: "https://i.imgur.com/dwlWYcI.png",
          brand: "Stone",
          oldPrice: 4899.9,
          price: 4017.9,
          available: true,
          details: {
            freeShipping: false,
          },
        },
        {
          id: 3,
          name: "Notebook StoneCO Prime 4GB RAM SSD 500GB Tela 15,6 Windows 10",
          image_url: "https://i.imgur.com/CpNAH6e.png",
          brand: "Stone",
          oldPrice: 2399.9,
          price: 2399.9,
          available: true,
          details: {
            freeShipping: true,
          },
        },
        {
          id: 4,
          name: "Notebook Linx Impulse Premium 4GB RAM SSD 500GB Tela 15,6 Windows 10",
          image_url: "https://i.imgur.com/zu9NkxS.png",
          brand: "Linx",
          oldPrice: 2569.9,
          price: 2569.9,
          available: false,
          details: {
            freeShipping: false,
          },
        },
        {
          id: 5,
          name: "Notebook Linx Impulse Premium 8GB RAM SSD 1TB Tela 15,6 Windows 10",
          image_url: "https://i.imgur.com/zu9NkxS.png",
          brand: "Linx",
          oldPrice: 4899.9,
          price: 4017.9,
          available: true,
          details: {
            freeShipping: false,
          },
        },
        {
          id: 6,
          name: "Smartphone Linx 4 GB RAM",
          image_url: "https://i.imgur.com/dwlWYcI.png",
          brand: "Linx",
          oldPrice: 2799.9,
          price: 2799.9,
          available: true,
          details: {
            freeShipping: true,
          },
        },
        {
          id: 7,
          name: "Notebook StoneCO Prime 8GB RAM SSD 500GB Tela 15,6 Windows 10",
          image_url: "https://i.imgur.com/CpNAH6e.png",
          brand: "Stone",
          oldPrice: 4399.9,
          price: 3871.9,
          available: true,
          details: {
            freeShipping: true,
          },
        },
      ],
    };
  },
};
</script>