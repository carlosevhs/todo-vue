<script setup>
    const props = defineProps (['cadastraTarefa','tarefaTemp','trocarfiltro','editaTarefaTemp']);
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                    type="text" placeholder="Digite aqui seu item" class="form-control">
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary"> Cadastrar </button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocarfiltro" class="form-control">
                    <option value="todas">Todos</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>