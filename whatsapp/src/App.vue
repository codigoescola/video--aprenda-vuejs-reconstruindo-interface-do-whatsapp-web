<template>
  <div id="app">
    <section class="section">
      <div class="container">
        <div class="columns janela-principal">

          <!-- Coluna Esquerda -->
          <div class="column is-3 lista-de-conversas">
            <div class="barra-superior"/>
            <item-lista-de-conversa 
              v-for="(conversa, indice) in conversas"
              :key="indice" 
              :nomeDoUsuario="conversa.usuario"
              :ultimaMensagem="conversa.mensagens.pop().conteudo"
            />
          </div>

          <!-- Coluna Direita -->
          <div class="column conversa-ativa">
            <!-- 1. Barra Superior -->
            <div class="barra-superior">
              <span>Usuario</span>
            </div>
            <!-- 2. Mensagens -->
            <div class="lista-mensagens">
              <mensagem-da-conversa-ativa/>
            </div>
            <!-- 3. Barra Inferior -->
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
import conversasIniciais from "./dados.js"
import ItemDaListaDeConversa from './components/ItemDaListaDeConversa.vue';
import MensagemDaConversaAtiva from './components/MensagemDaConversaAtiva.vue';
export default {
  name: "App",
  data: function(){
    return {
        conversas: conversasIniciais
      }
  },
  components: {
    "item-lista-de-conversa": ItemDaListaDeConversa,
    "mensagem-da-conversa-ativa": MensagemDaConversaAtiva
  }
};
</script>

<style>
.janela-principal{
    min-height: 1200px;
    box-shadow: 0 3rem 3rem -1rem rgba(10,10,10,.2);
}
</style>
