
<template>
  <center>
<h1>ESTO ES UN CONTADOR</h1>
<h1><P>{{ contador }}</P></h1>

<button @click="incrementar">Incrementar</button>
&nbsp; &nbsp;
<button @click="decrementar">Decrementar</button>
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

</style>
