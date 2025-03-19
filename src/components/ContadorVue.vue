
<template>

  <center>
<h1>ESTO ES UN CONTADOR</h1>
<h1><P>{{ contador }}</P></h1>

<button class="styled-button" @click="incrementar">INCREMENTAR</button>
&nbsp; &nbsp;
<button class="styled-button" @click="decrementar">DESCREMENTAR</button>
</center>
</template>




<script setup>
import { ref } from 'vue';


const contador = ref(0);
const incrementar = () => {
  contador.value+=5;
}

const decrementar = () => {
  contador.value-=5;
}

</script>





<style scoped>
p{
  color: blue;
}

.styled-button {
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  font-size: 12px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s;
}

.styled-button:hover {
  background-color: #0056b3;
  transform: scale(1.05);
}

.styled-button:active {
  transform: scale(0.95); 
}

</style>
