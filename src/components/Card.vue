<template>
  <div class="product">
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
    </div>
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
