<template>
  <div class="q-pa-md" style="width: 100%">
    <h3 class="text-gray-50 recomended">Рекомендации</h3>
    <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      swipeable
      animated
      control-color="primary"
      padding
      arrows
      height="300px"
      class="bg-background"
    >
      <q-carousel-slide :name="1" class="column no-wrap">
        <div
          class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
        >
          <q-img
            class="rounded-borders col-4 full-height"
            src="../../assets/Artboard5.svg"
          >
            <div class="absolute-bottom custom-caption flex flex-center">
              <div class="text-subtitle1">Создать сайт</div>
            </div>
          </q-img>
          <q-img
            class="rounded-borders col-4 full-height"
            src="../../assets/Artboard1.svg"
          >
            <div class="absolute-bottom custom-caption flex flex-center">
              <div class="text-subtitle1">Создать приложение</div>
            </div>
          </q-img>
          <q-img
            class="rounded-borders col-4 full-height"
            src="../../assets/Artboard2.svg"
          >
            <div class="absolute-bottom custom-caption flex flex-center">
              <div class="text-subtitle1">Бухгалтерия</div>
            </div>
          </q-img>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="2" class="column no-wrap">
        <div
          class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap"
        >
          <q-img
            class="rounded-borders col-6 full-height"
            src="../../assets/Artboard3.svg"
          >
            <div class="absolute-bottom custom-caption flex flex-center">
              <div class="text-subtitle1">Дизайн</div>
            </div>
          </q-img>
          <q-img
            class="rounded-borders col-6 full-height"
            src="../../assets/Artboard4.svg"
          >
            <div class="absolute-bottom custom-caption flex flex-center">
              <div class="text-subtitle1">SEO продвижение</div>
            </div>
          </q-img>
          <!-- <q-img
            class="rounded-borders col-4 full-height"
            src="../../assets/Artboard1.svg"
          >
            <div class="absolute-bottom custom-caption flex flex-center">
              <div class="text-subtitle1">Famous City</div>
            </div>
          </q-img> -->
        </div>
      </q-carousel-slide>
    </q-carousel>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    return {
      slide: ref(1),
    };
  },
};
</script>

<style></style>
