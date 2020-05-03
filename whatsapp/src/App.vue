<template>
  <div id="app">
    <section class="section">
      <div class="container">
        <div class="columns janela-principal">

          <!-- Coluna Esquerda -->
          <div class="column is-3 lista-de-conversas">
            <div class="barra-superior"  />
            <item-lista-de-conversa 
              v-for="(conversa, indice) in conversas"
              :key="indice" 
              :mensagemAtiva="indice == indiceAtivo"
              :nomeDoUsuario="conversa.usuario"
              :ultimaMensagem="conversa.mensagens[0].conteudo"
              v-on:click.native="indiceAtivo=indice"
            />
          </div>

          <!-- Coluna Direita -->
          <div class="column conversa-ativa">
            <!-- 1. Barra Superior -->
            <div class="barra-superior">
              <span>{{conversas[indiceAtivo].usuario}}</span>
            </div>
            <!-- 2. Mensagens -->
            <div class="lista-mensagens">
              <mensagem-da-conversa-ativa 
                :conteudo="mensagem.conteudo"
                :horario="mensagem.horario"
                :verde="mensagem.verde"
                v-for="(mensagem, indice_) in conversas[indiceAtivo].mensagens"
                :key="indice_" 
              />
            </div>
            <!-- 3. Barra Inferior -->
            <div class="barra-inferior">
              <input type="text" class="input"  v-on:keyup.enter="enviarMensagem" placeholder="Insira sua mensagem" v-model="conteudoASerEnviado">
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
        conversas: conversasIniciais,
        indiceAtivo: 0,
        conteudoASerEnviado: "",
      }
  },
  components: {
    "item-lista-de-conversa": ItemDaListaDeConversa,
    "mensagem-da-conversa-ativa": MensagemDaConversaAtiva
  },
  methods: {
    enviarMensagem: function(){
      let horarioAtual = new Date().getHours() + ":" + new Date().getMinutes();

      let novaMensagem = {
        horario: horarioAtual,
        conteudo: this.conteudoASerEnviado,
        verde: true
      };

      this.conversas[this.indiceAtivo]
        .mensagens
        .push(novaMensagem);

      this.conteudoASerEnviado = "";
    }
  }

};
</script>

<style>
.janela-principal{
    min-height: 1200px;
    box-shadow: 0 3rem 3rem -1rem rgba(10,10,10,.2);
}
/* Coluna Esquerda */
.lista-de-conversas{
    padding: 0;
    background:white;
}
</style>
