<script setup>
import { ref } from 'vue';

// ref() cria dados reativos, para acessar esses dados precisamos usar o .value

// variável inicial
const numero = ref(0)

// função de aumentar o número
function aumentar() {
    numero.value++
}

// função de diminuir o número
function diminuir() {
    // sem impedir que seja negativo
    // numero.value--

    // limitando aos naturais
    if(numero.value > 0){
        numero.value--
    }
}
</script>

<template>
    <h1>Contador</h1>
    <h2>{{ numero }}</h2>
    <!-- clique com atalho -->
    <button @click="aumentar">+</button>
    <!-- a forma sem atalho -->
    <button v-on:click="diminuir">-</button> 
</template>

<style scoped>

</style>
