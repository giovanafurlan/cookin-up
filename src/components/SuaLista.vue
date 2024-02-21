<script lang="ts">
export default {
  props: {
    ingredientes: { type: Object, required: true },
  },
};
</script>

<template>
  <section>
    <span class="subtitulo-lg sua-lista-texto"> Sua lista: </span>

    <ul v-if="ingredientes.length" class="ingredientes-sua-lista">
      <li v-for="ingrediente in ingredientes" :key="ingrediente">
        <Tag :texto="ingrediente" ativa="" />
      </li>
    </ul>
    <p v-else class="paragrafo lista-vazia">
      <img
        src="../assets/imagens/icones/lista-vazia.svg"
        alt="Ícone de pesquisa"
      />
      Sua lista está vazia, selecione ingredientes para iniciar.
    </p>
  </section>
</template>
