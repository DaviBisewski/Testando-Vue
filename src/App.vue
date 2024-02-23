<script setup>
import {ref} from 'vue'
const contador = ref(0)

function decrementar() {
  contador.value--

if(contador.value < 0){
  contador.value++
}
}

function incrementar() {
  contador.value++
}

function limpar() {
  contador.value=0
}

</script>

<template>
 <button @click="incrementar">+</button>
 <button @click="decrementar">-</button>
  <p>Valor do contador: {{ contador }} </p>
  <button @click="limpar">Limpar</button>
</template>

<style scoped>
  button{
    background-color: #212121;
    color: #fff;
    font-weight: 600;
    border-radius: 20px;
    border: 2px solid #212121;
    font-size: 20px;
    padding: 10px;
    margin: 10px;
    transition: all 2s ease-in-out;
  }

  button:hover{
    transform: rotate(990deg);
    background-color: #fff;
    color: #212121;
  }
</style>
