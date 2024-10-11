<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
      <div class="row">
        <div class="col">
      <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required type="text" placeholder="Digíte aqui a descrição da tareda" class="form-control">
    </div>
    <div class="col-md-2">
      <button class="btn btn-primary" type="submit">Cadastar</button>
    </div>
    <div class="col-md-2">
      <select @change="props.trocarFiltro" class="form-control">
        <option value="todas">Todas</option>
        <option value="pendentes">Pendentes</option>
        <option value="finalizadas">Finalizadas</option>
      </select>
    </div>
      </div>
  </form>
</template>