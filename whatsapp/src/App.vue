<template>
  <div id="app">
    <section class="section">
      <div class="container">
        <div class="columns janela-principal">
          <div class="column is-3 lista-de-conversas">
            <div class="barra-superior"/>
            <div class="item">
              <div class="title is-6">Usuario</div>
              <div class="subtitle is-6">Conversa</div>
            </div>
            <div class="item">
              <div class="title is-6">Usuario</div>
              <div class="subtitle is-6">Conversa</div>
            </div>
          </div>
          <div class="column conversa-ativa">
            <div class="barra-superior">
              <span>Usuario</span>
            </div>
            <div class="lista-mensagens">
              <div class="mensagem">
                Esta é uma mensagem do usuário de lá.
                <span>10:15</span>
              </div>
              <div class="mensagem">
                Esta é uma mensagem do usuário de lá.
                <span>10:15</span>
              </div>
              <div class="mensagem verde">
                Esta é uma mensagem do usuário de lá.
                <span>10:15</span>
              </div>
            </div>
            <div class="barra-inferior">
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
