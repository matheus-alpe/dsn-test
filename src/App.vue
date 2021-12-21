<template>
  <div id="app">
    <header>
      <h1>Linx & Stone Store</h1>
      <h2>Um mundo de possibilidades para o seu negócio</h2>
    </header>

    <main>
      <nav class="navigation">
        <form class="search" action="#">
          <input type="text" placeholder="Buscar produto">
          <button type="submit">Buscar</button>
        </form>

        <div>
          <label for="order-by">Filtrar por:</label>
          <select name="order-by" id="order-by">
            <option value="Maior valor">Maior Valor</option>
            <option value="Menor valor">Menor Valor</option>
          </select>
        </div>
      </nav>
      
      <section class="products">
        <ProductCard 
          v-for="product in products" 
          :key="product.id"
          :product="product"
        />
      </section>

      <form class="newsletter" action="#">
        <h3>Quer receber dicas para organizar melhor a sua rotina? Cadastre-se!</h3>

        <div>
          <div>
            <label for="name">nome</label>
            <input type="text" id="name" placeholder="Digite seu nome" required>
          </div>

          <div>
            <label for="email">e-mail</label>
            <input type="email" id="email" placeholder="Digite seu e-mail" required>
          </div>

          <div>
            <button type="submit">Cadastrar</button>
          </div>
        </div>

      </form>

      <section class="about">
        <div class="about__logo">
          <img src="@/assets/linx-stone.png" alt="Logo Linx Stone">
        </div>

        <div class="about__text">
          <p>A Linx é uma empresa brasileira especialista em tecnologia para o varejo. Líder no mercado de software de gestão, com 45,6% de market share do mercado varejista, conforme atesta o IDC.</p>
          <p>Toda a expertise da Linx na jornada de compra é transformada em insights fundamentais para atingir o que os varejistas mais esperam: fidelizar seus consumidores e atingir resultados concretos e relevantes.</p>
          <p>Com capital aberto na B3 desde 2013, a Linx também se tornou a primeira empresa brasileira de software com capital aberto na NYSE, em 2019. A empresa possui mais de 3,5 mil colaboradores distribuídos entre sua sede em São Paulo, 15 filiais pelo Brasil e 5 países da América. Para saber mais, acesse linx.com.br/imprensa.</p>
        </div>
      </section>
    </main>

    <footer>
      <p>Testando suas habilidades em HTML e CSS.</p>
      <p>Linx Impulse 2022</p>
      <p>Teste ficcional!</p>
    </footer>

  </div>
</template>

<script>
import ProductCard from './components/ProductCard.vue'

export default {
  name: 'App',
  components: {
    ProductCard
  },
  data() {
    return {
      products: [
        {
            "id": 1,
            "name": "Notebook Linx Impulse Premium 8GB RAM SSD 500GB Tela 15,6 Windows 10",
            "image_url": "https://i.imgur.com/zu9NkxS.png",
            "brand": "Linx",
            "oldPrice": 4199.90,
            "price": 3569.90,
            "available": true,
            "details": {
                "freeShipping": true
            }
        },
        {
            "id": 2,
            "name": "Smartphone Linx 6 GB RAM",
            "image_url": "https://i.imgur.com/dwlWYcI.png",
            "brand": "Stone",
            "oldPrice": 4899.90,
            "price": 4017.90,
            "available": true,
            "details": {
                "freeShipping": false
            }
        },
        {
            "id": 3,
            "name": "Notebook StoneCO Prime 4GB RAM SSD 500GB Tela 15,6 Windows 10",
            "image_url": "https://i.imgur.com/CpNAH6e.png",
            "brand": "Stone",
            "oldPrice": 2399.90,
            "price": 2399.90,
            "available": true,
            "details": {
                "freeShipping": true
            }
        },
        {
            "id": 4,
            "name": "Notebook Linx Impulse Premium 4GB RAM SSD 500GB Tela 15,6 Windows 10",
            "image_url": "https://i.imgur.com/zu9NkxS.png",
            "brand": "Linx",
            "oldPrice": 2569.90,
            "price": 2569.90,
            "available": false,
            "details": {
                "freeShipping": false
            }
        },
        {
            "id": 5,
            "name": "Notebook Linx Impulse Premium 8GB RAM SSD 1TB Tela 15,6 Windows 10",
            "image_url": "https://i.imgur.com/zu9NkxS.png",
            "brand": "Linx",
            "oldPrice": 4899.90,
            "price": 4017.90,
            "available": true,
            "details": {
                "freeShipping": false
            }
        },
        {
            "id": 6,
            "name": "Smartphone Linx 4 GB RAM",
            "image_url": "https://i.imgur.com/dwlWYcI.png",
            "brand": "Linx",
            "oldPrice": 2799.90,
            "price": 2799.90,
            "available": true,
            "details": {
                "freeShipping": true
            }
        },
        {
            "id": 7,
            "name": "Notebook StoneCO Prime 8GB RAM SSD 500GB Tela 15,6 Windows 10",
            "image_url": "https://i.imgur.com/CpNAH6e.png",
            "brand": "Stone",
            "oldPrice": 4399.90,
            "price": 3871.90,
            "available": true,
            "details": {
                "freeShipping": true
            }
        }
      ]
    }
  }
}
</script>