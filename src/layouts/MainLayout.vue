<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-deep-purple-10 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="~src/assets/icone2.png">
          </q-avatar>
          Lista de Tarefas
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

       <q-footer elevated class="bg-deep-purple-10 text-white">
      <q-toolbar>
        <q-toolbar-title>

        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>
