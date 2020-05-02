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
            <div class="top-bar"/>
            <div class="bottom-bar">
              <input type="text" placeholder="Insira sua mensagem">
            </div>
            <!-- Conversa Ativa -->
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
