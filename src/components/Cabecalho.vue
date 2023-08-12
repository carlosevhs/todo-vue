<script setup>
    const props = defineProps(['tarefasPedentes'])
</script>
<template>
    <header class="p-5 mb-4 mt-4 bg-info rounded-3">
        <h1>LISTA DE COMPRAS</h1>
        <p>
            Você possui {{ props.tarefasPedentes }} itens pendentes
        </p>
    </header>
</template>