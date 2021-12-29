<template>
  <div class="product" :class="{ 'unavailable': !product.available }" >
    <div class="info">
      <div class="thumbnail">
        <img
          :src="product.image_url"
          :alt="product.name"
          referrerpolicy="no-referrer"
        />
      </div>

      <div class="content">
        <p class="name">{{ product.name }}</p>

        <div class="prices">
          <span class="oldprice">{{ formatPrice(product.oldPrice) }}</span>
          <span class="price">{{ formatPrice(product.price) }}</span>
        </div>

        <p class="installment">10x de {{ formatPrice(installment) }} sem juros</p>
        <a :href="product.image_url" target="_blank" class="view">Ver produto</a>
      </div>
    </div>
    <a :href="product.image_url" target="_blank" class="view overlay">Ver produto</a>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    product: Object,
  },
  computed: {
    installment() {
      return this.product.price / 10;
    },
  },
  methods: {
    formatPrice(value) {
      return value.toLocaleString("pt-BR", {
        style: "currency",
        currency: "BRL",
      });
    },
  },
};
</script>
