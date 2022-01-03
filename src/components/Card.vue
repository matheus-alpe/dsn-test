<template>
  <div class="product" :class="{ 'unavailable': !product.available }" >
    <div class="info">
      <div
        class="flags"
        v-if="product.available"
      >
        <span
          class="flag discount"
          v-if="discount"
        >
          {{ discount }}% OFF
        </span>

        <span
          v-if="product.details.freeShipping"
          class="flag free-shipping"
        >
          Frete Grátis
        </span>
      </div>
      <div class="thumbnail">
        <img
          :src="product.image_url"
          :alt="product.name"
          referrerpolicy="no-referrer"
        />
      </div>

      <div class="content">
        <p class="name">{{ product.name }}</p>

        <template v-if="product.available">
          <div
            class="prices"
            :class="{ 'minimal': !discount }"
          >
            <div class="oldPrice-container">
              <span
                class="oldprice" 
                v-if="discount"
              >
                {{ formatPrice(product.oldPrice) }}
              </span>
            </div>

            <span class="price">{{ formatPrice(product.price) }}</span>
          </div>

          <p class="installment">10x de {{ formatPrice(installment) }} sem juros</p>
          <a :href="product.image_url" target="_blank" class="view">Ver produto</a>
        </template>

        <div
          v-else
          class="unavailable-message"
        >
          <p>Produto Indisponível</p>
        </div>
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
    
    discount() {
      const discount = this.product.price / this.product.oldPrice;
      if (discount === 1) return false;
      return Math.trunc((1 - discount) * 100);
    }
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
