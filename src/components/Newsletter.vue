<template>
  <div class="newsletter">
    <h3>Quer receber dicas para organizar melhor a sua rotina? Cadastre-se!</h3>

    <form action="#">
      <div class="input-group">
        <label for="name">nome</label>
        <input type="text" id="name" placeholder="Digite seu nome" required />
      </div>

      <div class="input-group">
        <label for="email">e-mail</label>
        <input
          type="email"
          id="email"
          placeholder="Digite seu e-mail"
          required
        />
      </div>

      <div class="button-group">
        <button type="submit">Cadastrar</button>
      </div>
    </form>
  </div>
</template>