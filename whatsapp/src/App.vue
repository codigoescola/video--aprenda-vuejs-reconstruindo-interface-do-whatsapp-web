<template>
  <div id="app">
    <section class="section">
      <div class="container">
        <div class="columns principal">
          <div class="column is-3 conversas">
            <div class="top-bar"/>
            <div class="content conversa">
              <div class="title is-6">Usuario</div>
              <div class="subtitle is-6">Conversa</div>
            </div>
            <div class="content conversa">
              <div class="title is-6">Usuario</div>
              <div class="subtitle is-6">Conversa</div>
            </div>
          </div>
          <div class="column conversa-ativa">
            <div class="top-bar">
              <span>Usuario</span>
            </div>
            <div class="mensagens">
            <div class="mensagem-usuario">
              Esta é uma mensagem do usuário de lá.
              <span>10:15</span>
            </div>
            <div class="mensagem-usuario">
              Esta é uma mensagem do usuário de lá.
              <span>10:15</span>
            </div>
            <div class="mensagem-usuario local">
              Esta é uma mensagem do usuário de lá.
              <span>10:15</span>
            </div>
            </div>
            <div class="bottom-bar">
              <input type="text" class="input" placeholder="Insira sua mensagem">
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {}
};
</script>

<style>
</style>
