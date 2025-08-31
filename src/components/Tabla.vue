<template>
    <table v-if="visible" class="table">
        <thead>
            <tr>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">Fecha nacimiento</th>
                <th scope="col">Edad</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(nombre, index) in nombre2" :key="index">
                <td>{{ nombre }}</td>
                <td>{{ apellido2[index] }}</td>
                <td>{{ fechaNacimiento2[index] }}</td>
                <td>{{ edad2[index] }}</td>
            </tr>
        </tbody>
    </table>
</template>

<script setup>
import { ref } from 'vue'
const nombre2 = ref(['León', 'Angela', 'Perico'])
const apellido2 = ref(['Pizarro', 'Gonzalez', 'Lopez'])
const fechaNacimiento2 = ref(['17-02-2012', '25-12-2010', '01-01-2000'])
const edad2 = ref([13, 15, 25])

const props = defineProps({
    visible: {
        type: Boolean,
        default: false
    }
})
</script>