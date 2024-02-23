<script setup>
import {ref} from 'vue'
const contador = ref(0)

function incrementar() {
  contador.value++
}

function decrementar() {
  contador.value--
}

</script>

<template>
 <button @click="incrementar++">+</button>
 <button @click="decrementar--">-</button>
  <p>Valor do contador: {{ contador }} </p>
</template>

<style scoped>

</style>
