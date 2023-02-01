<template>
  <q-layout view="hHh lpR fFf" class="bg-background">
    <v-header />
    <q-drawer v-model="leftDrawerOpen" show-if-above bordered content-class="bg-grey-1">
      <q-list>
      </q-list>
      </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",
  components: {
    "v-header": async () => await import("components/header.vue")
  },
  data() {
    return {
      leftDrawerOpen: false,
    };
  }
};
</script>
