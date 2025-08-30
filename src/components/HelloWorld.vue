
<script setup>
import { defineProps } from 'vue'
const props = defineProps({
  msg: {
    type: String,
    required: true,
  },
  mostrarTabla: {
    type: Function,
    required: true,
  },
  ocultarTabla: {
    type: Function,
    required: false,
  }
})


</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
      <br>
  <p>Aquí va la <button @click="props.mostrarTabla" class="btn btn-link">Tabla</button> de tres personas</p>
  <!-- <button v-if="visible" class="btn btn-outline-info" @click="props.ocultarTabla">Ocultar</button> -->
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

p {
  font-size: 1.2rem;
  text-align: center;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
