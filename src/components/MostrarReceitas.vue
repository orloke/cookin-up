<script lang="ts">
import BotaoPrincipal from './BotaoPrincipal.vue'
export default {
  components: { BotaoPrincipal },
  emits:['editarLista']
}
</script>

<template>
  <BotaoPrincipal texto="Editar Lista" @click="$emit('editarLista')" />
</template>
