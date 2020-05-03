<template>
  <div class="mensagem" v-bind:class="{verde: verde}">
    {{conteudo}}
    <span>{{horario}}</span>
  </div>
</template>
<script>
export default {
  name: "MensagemDaConversaAtiva",
  props: ['conteudo', 'horario', 'verde']
};
</script>