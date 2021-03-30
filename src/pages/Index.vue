<template>
  <q-page padding>

    <q-input v-model="novaTarefa" label="O que você quer fazer?" />

    <q-btn
      class="full-width"
      color="deep-purple-10"
      icon="add"
      label="Adicioniar Tarefa"
      @click="adicionarTarefaNaLista()" />

    <q-list bordered separator class="espacado-em-cima">

      <q-item clickable v-ripple
       v-for="tarefa in tarefas"
       @click="alternarFinalizacaoDaTarefa(tarefa)">

        <q-item-section
          :class="{ 'tarefa-finalizada': tarefa.finalizada }">

          {{ tarefa.descricao }}
          </q-item-section>
      </q-item>

    </q-list>


  </q-page>
</template>

<style scoped>
 .espacado-em-cima {
   margin-top: 30px;
 }

 .tarefa-finalizada {
   text-decoration: line-through;
 }


</style>

<script>
export default {
  name: 'PageIndex',
  data()  {
    return {
      novaTarefa: '',
      tarefas: [],

    };
  },
  methods: {
    adicionarTarefaNaLista() {
      const tarefa = { descricao: this.novaTarefa, finalizada: false };

      this.tarefas.push(tarefa);

      this.novaTarefa = '';
    },

    alternarFinalizacaoDaTarefa(tarefa) {
      tarefa.finalizada = !tarefa.finalizada;

    },

  },


}
</script>
