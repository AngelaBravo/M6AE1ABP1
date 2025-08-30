<script setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import Tabla from './components/Tabla.vue'

const mostrarTabla = ref(false)
function mostrarTablaFn() {
  mostrarTabla.value = true
}

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/Favicon3.jpg" height="125" />

    <div class="wrapper">
  <HelloWorld msg="M6AE1-ABP1" :mostrarTabla="mostrarTablaFn" />
    </div>
  </header>

  <main>
    <TheWelcome />
    <br>
  <Tabla :visible="mostrarTabla" />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
