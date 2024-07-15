<script setup>

import { computed, ref} from 'vue';

//const props = defineProps(['title','content'])

const props = defineProps({
titel:{
    type:String,
    required:true
},

content:{
    type:String,
    default:'Valor padrão do texto da caixa...'
}
})

const showContent = ref(false)
const textButton = computed(()=>(showContent.value? 'Esconder':'Mostrar'))
</script>

<template>

<div>
<button @click="showContent=!showContent">mostrar</button>
<div v-if="showContent" class="ExpandBox">
<h1>{{ title }}</h1>
<p>{{ content }}</p>
</div>
</div>

</template>

<style scoped>

.ExpandBox{

    height: 100%;
    padding: 20px;
    border: 1px solid black;
    border-radius: 10px;
    box-shadow: 3px 3px 2px 2px gray;
}

</style>