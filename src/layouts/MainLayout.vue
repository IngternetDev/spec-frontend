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
          <div class="sidebar__main">
            <h1 class="text-gray-200 q-ml-md text-uppercase">Все професии</h1>
            <q-list class="q-mt-md">
              <q-item
                v-for="(item, index) in items"
                :key="item.text"
                clickable
                v-ripple
                content-class="bg-gray-100"
                class="sidebar__item"
                :class="[active === index ? 'bg-gray-300' : '']"
                @click="active = index"
              >
                <q-item-section
                  class="text-gray-100"
                  :class="{ active: active === index }"
                >
                  {{ item.text }}
                </q-item-section>
                <q-item-section avatar>
                  <img :src="require('assets/sidebarIcon.svg')" alt="" />
                </q-item-section>
                <span class="sidebar__count text-gray-200 text-center">
                  {{ item.count }}
                </span>
              </q-item>
            </q-list>
          </div>
          <div class="sidebar__footer">
            <div class="sidebar__footer-info">
              <span class="text-gray-200 text-center"> Правила </span>
              <span class="text-gray-200 text-center q-ml-md">
                Сообщества
              </span>
            </div>
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
      { text: "Все подряд", count: 54 },
      { text: "Front-end", count: 12 },
      { text: "Back-end", count: 7 },
      { text: "UX/UI", count: 6 },
      { text: "Брендинг", count: 8 },
      { text: "QA - тестирование", count: 4 },
      { text: "SMM", count: 12 },
      { text: "SEO", count: 5 },
      { text: "1-С", count: 5 },
    ],

    active: 0,
  }),
};
</script>
