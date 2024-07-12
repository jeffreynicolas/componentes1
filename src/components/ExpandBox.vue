<script setup>

import { ref} from 'vue';

const showContent = ref(false)
</script>

<template>

<div>
<button @click="showContent=!showContent">mostrar</button>
<div v-if="showContent" class="ExpandBox">
Murilooooooooooooooooooooooooo
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