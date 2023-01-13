<template>
  <q-layout view="hHh lpR fFf" class="bg-background">
    <v-header />
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-gray-500"
    >
      <q-list>
        <div class="sidebar">
          <div class="q-pa-md" style="max-width: 274px">
            <q-title class="text-gray-200 q-ml-md text-uppercase"
              >все профессии</q-title
            >
            <q-list class="q-mt-md">
              <q-items>
                <q-item
                  v-for="(item, index) in items"
                  :key="item.id"
                  text-color="white"
                  clickable
                  v-ripple
                  content-class="bg-gray-100"
                  class="sidebar__item"
                  :class="[active === index ? 'bg-gray-300' : '']"
                  @click="setActive(index)"
                >
                  <q-item-section
                    class="text-gray-100"
                    :class="{ active: active === index }"
                  >
                    {{ item.text }}
                  </q-item-section>
                  <q-item-section avatar>
                    <img src="../assets/sidebarIcon.svg" alt="" />
                  </q-item-section>
                  <text-overline
                    class="sidebar__amount text-gray-200 text-center"
                  >
                    {{ item.amount }}
                  </text-overline>
                </q-item>
              </q-items>
              <q-separator></q-separator>
            </q-list>
          </div>
          <div class="sidebar__footer">
            <text-overline class="text-gray-200 text-center">
              Правила
            </text-overline>
            <text-overline class="text-gray-200 text-center q-ml-md">
              Сообщества
            </text-overline>
            <span class="text-gray-200">Ingternet © 2022</span>
          </div>
        </div>
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
    "v-header": async () => await import("components/header.vue"),
  },
  data: () => ({
    leftDrawerOpen: false,
    items: [
      { id: 1, text: "Все подряд", amount: 54 },
      { id: 2, text: "Front-end", amount: 12 },
      { id: 4, text: "Back-end", amount: 7 },
      { id: 5, text: "UX/UI", amount: 6 },
      { id: 6, text: "Брендинг", amount: 8 },
      { id: 7, text: "QA - тестирование", amount: 4 },
      { id: 8, text: "SMM", amount: 12 },
      { id: 9, text: "SEO", amount: 5 },
      { id: 10, text: "1-С", amount: 5 },
    ],

    active: 0,
  }),
  methods: {
    setActive: function (i) {
      this.active = i;
    },
  },
};
</script>
