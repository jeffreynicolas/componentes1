<script setup>

import { ref} from 'vue';

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
</script>

<template>

<div>
<button @click="showContent=!showContent">mostrar</button>
<div v-if="showContent" class="ExpandBox">
<h1>{{ props.title }}</h1>
<p>{{ props.content }}</p>
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