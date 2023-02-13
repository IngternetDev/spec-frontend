<template>
  <q-page class="flex">
    <carousel />
  </q-page>
</template>

<script>
import carousel from "./Index/carousel.vue";

export default {
  name: "PageIndex",
  components: {
    carousel,
  },
};
</script>
