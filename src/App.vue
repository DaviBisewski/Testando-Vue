<script setup>
const nome = 'Davi e Murilo'
const idade = '16'

function inverter(texto) {
  return texto.split('').reverse().join('').toUpperCase()
}

function saudacao() {
  return `Olá, ${nome}!`
}

import { ref } from 'vue'
const contador = ref(0)

function decrementar() {
  contador.value--

  if (contador.value < 0) {
    contador.value++
  }
}

function incrementar() {
  contador.value++
}

</script>

<template>
  <div id="info">
    <h1>Exemplo 1 - Mostrando informações na tela</h1>
    <hr>
    <p>Nome: {{ nome }} </p>
    <p>Idade: {{ idade }} anos</p>
    <hr>
    <p>Para completar 50 anos faltam: {{ 50 - idade }} anos</p>
    <p>O nome tem {{ nome.length }} caracteres</p>
    <p>O nome invertido é: {{ inverter(nome) }} </p>
    <hr>
    <p> Exemplo de saudação usando função</p>
    <p> {{ saudacao() }} </p>
  </div>
  <br>
  <div id="contador">
    <button @click="incrementar">+</button>
    <button @click="decrementar">-</button>

    <p>Valor do contador: {{ contador }} </p>
    <div v-if="contador < 10" class="red">
      O número é menor que 10
    </div>
    <div v-else-if="contador > 10" class="green">
      O número é maior que 10
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  font-weight: 400;
}

#info {
  background-color: rgb(41, 41, 41);
  border-radius: 20px;
  padding: 15px;
  min-width: 650px;
  color: rgb(255, 255, 255);
}

h1 {
  text-align: center;
}

#contador {
  margin-top: 35px;
  background-color: rgb(41, 41, 41);
  border-radius: 20px;
  padding: 15px;
  min-width: 650px;
  color: black;
}

button {
  width: 30px;
  height: 20px;
  border-radius: 30px;
  border: 1px solid black;
}

.red {
  background-color: rgb(230, 48, 48);
  color: black;
}

.green {
  background-color: rgb(44, 180, 44);
  color: black;
}
</style>