<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-brown-4 text-black text-right">

        <q-toolbar-title>
          Sura App
        </q-toolbar-title>

        <q-btn
          flat
          dense
          round
          icon="menu_book"
        />

      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',

  data () {
    return {

    }
  }
}
</script>
