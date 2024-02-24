<script lang="ts">
import type ICategoria from '@/interfaces/ICategoria'
import type { PropType } from 'vue'

export default {
  props: {
    categoria: { type: Object as PropType<ICategoria>, required: true },
  },
}
</script>

<template>
  <article class="categoria">
    <header class="categoria__cabecalho">
      <img
        :src="`/imagens/icones/categorias_ingredientes/${categoria.imagem}`"
        alt=""
        class="categoria__imagem"
      />

      <h2 class="paragrafo-lg categoria__nome">{{ categoria.nome }}</h2>
    </header>

    <ul class="categoria__ingredientes">
      <li v-for="ingrediente in categoria.ingredientes" :key="ingrediente">
        {{ ingrediente }}
      </li>
    </ul>
  </article>
</template>
