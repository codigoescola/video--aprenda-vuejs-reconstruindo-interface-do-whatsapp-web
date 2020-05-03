<template>
  <div class="item" v-bind:class="{ativo: mensagemAtiva}">
    <div class="title is-6">{{nomeDoUsuario}}</div>
    <div class="subtitle is-6">{{ultimaMensagem}}</div>
  </div>
</template>

<script>
export default {
  name: 'ItemDaListaDeConversa',
  props:['nomeDoUsuario','ultimaMensagem','mensagemAtiva'],
}
</script>

<style>
  .item{
      border-top: 1px solid #F2F2F2;
      border-bottom: 1px solid #F2F2F2;
      padding: 15px 30px;
      margin-bottom: 0 !important;
  }
  .item:hover{
      background: #F5F5F5;
      cursor: pointer;
  }
  .item.ativo{
    background: rgb(235, 235, 235);
  }
</style>