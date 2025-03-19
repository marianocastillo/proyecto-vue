<template>
  <center>
  <div>

  <br><br>
    <h2>Lista de Tareas</h2>
    <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea">

      <p v-for="(tarea, index) in tareas" :key="index">
      <br> {{ tarea  }}
      &nbsp;
      <button class="styled-button" @click="borrarTarea">BORRAR</button>
      </p>

</div>
</center>
</template>


<script setup>
import { ref } from 'vue';


const tareas = ref([]);
const nuevaTarea = ref('');
const addTarea = () => {
  tareas.value.push(nuevaTarea.value);
  nuevaTarea.value = '';
}

const borrarTarea = (index) =>{
tareas.value.splice(index, 1);

}
</script>



<style>
.styled-button {
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  font-size: 12px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.2s;
}

.styled-button:hover {
  background-color: #b30000;
  transform: scale(1.05);
}

.styled-button:active {
  transform: scale(0.95);
}
</style>
