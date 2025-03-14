<script lang="ts">
export default{
    props:{ //Objeto com a propiedade texto 
        texto: {type: String, required:true}, //ela é obrigatória. Devemos sempre passá-la se o componente de tag for consumido.
        ativa: Boolean
    }
}
</script>

<template>
    <span class="tag" :class="{ativa}">
        {{ texto }}
    </span>
</template>

<style scoped>
.tag{
  display: inline-block;
  border-radius: 0.5rem;
  min-width: 4.25rem;
  padding: 0.5rem;
  text-align: center;
  transition: 0.2s;
  color: var (--cinza);
  background: var(--cinza-claro);
  font-weight: 400;
}

.tag.ativa {
  color: var(--creme, #FFFAF3);
  background: var(--coral, #F0633C);
  font-weight: 700;
}
</style>