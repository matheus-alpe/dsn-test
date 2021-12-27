<template>
  <nav class="filters">
    <form class="search" action="#">
      <input type="text" placeholder="Buscar produto" />
      <button type="submit">Buscar</button>
    </form>

    <div class="order-by">
      <label for="order-by">Filtrar por:</label>
      <select name="order-by" id="order-by">
        <option value="Maior valor">Maior Valor</option>
        <option value="Menor valor">Menor Valor</option>
      </select>
    </div>
  </nav>
</template>