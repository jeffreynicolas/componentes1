<script setup>
import ExpandBox from './components/ExpandBox.vue'

const ti

</script>

<template>
 <h1>componentes</h1>
 <expand-box : title="title"/>
 <expand-box v-bind='caixa in caixas' : key="caixa.id" v-bind="caixa"/>

 <--!<ExpandBox  title="Caixa1" content="Conteudo secreto"/>
  <ExpandBox  title="Caixa2"/>
  <expandbox  title="Caixa3" Quanty="20"/>--!>
</template>

<style scoped></style>
