<template>
    <table v-if="visible" class="table">
        <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">Fecha nacimiento</th>
                <th scope="col">Edad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">1</th>
                <td>{{ nombre2[0] }}</td>
                <td>{{ apellido2[0] }}</td>
                <td>{{ fechaNacimiento2[0] }}</td>
                <td>{{ edad2[0] }}</td>
            </tr>
            <tr>
                <th scope="row">2</th>
                <td>{{ nombre2[1] }}</td>
                <td>{{ apellido2[1] }}</td>
                <td>{{ fechaNacimiento2[1] }}</td>
                <td>{{ edad2[1] }}</td>
            </tr>
            <tr>
                <th scope="row">3</th>
                <td>{{ nombre2[2] }}</td>
                <td>{{ apellido2[2] }}</td>
                <td>{{ fechaNacimiento2[2] }}</td>
                <td>{{ edad2[2] }}</td>
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