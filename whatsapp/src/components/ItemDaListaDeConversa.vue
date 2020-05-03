<template>
  <div class="item">
    <div class="title is-6">{{nomeDoUsuario}}</div>
    <div class="subtitle is-6">{{ultimaMensagem}}</div>
  </div>
</template>

<script>
export default {
  name: 'ItemDaListaDeConversa',
  props:['nomeDoUsuario','ultimaMensagem'],
}
</script>