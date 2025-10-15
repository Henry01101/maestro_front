<template>
    <form class="max-w-md mx-auto bg-white p-6 rounded shadow-md">
        <div class="mb-4">
            <label class="block text-gray-700 font-bold mb-2" for="nombre">
                Nombre
            </label>
            <input
                id="nombre"
                type="text"
                v-model="form.nombre"
                class="w-full px-3 py-2 border rounded focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="Ingresa tu nombre"
            />
        </div>
        <div class="mb-4">
            <label class="block text-gray-700 font-bold mb-2" for="email">
                Email
            </label>
            <input
                id="email"
                type="email"
                v-model="form.email"
                class="w-full px-3 py-2 border rounded focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="Ingresa tu email"
            />
        </div>
        <div class="mb-6">
            <label class="block text-gray-700 font-bold mb-2" for="edad">
                Edad
            </label>
            <input
                id="edad"
                type="number"
                v-model="form.edad"
                class="w-full px-3 py-2 border rounded focus:outline-none focus:ring-2 focus:ring-blue-500"
                placeholder="Ingresa tu edad"
            />
        </div>
        <button
            type="submit"
            class="w-full bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700 transition"
            @click.prevent="submitForm"
        >
            Enviar
        </button>
    </form>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
    nombre: '',
    email: '',
    edad: ''
})

function submitForm() {
    // Aquí puedes manejar el envío del formulario
    console.log(form)
}
</script>