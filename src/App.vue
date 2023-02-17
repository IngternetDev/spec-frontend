<template>
  <div id="q-app">
    <specialist
      v-for="specialist in specialists"
      :key="specialist.article"
      :specialist_data="specialist"
    />
    <router-view />
  </div>
</template>

<script>
import specialist from "./components/specialist.vue";

export default {
  name: "App",
  components: { specialist },
  data() {
    return {
      specialists: [
        {
          image: "1.png",
          name: "Jimmy Hudson",
          work: "UX/UI",
          online: true,
          about:
            "Я хочень хороший человек. Без вредных привычек. Не курю, не пью, людей не обижаю",
          social: {
            twitter: "https://www.youtube.com/",
            vk: "https://www.youtube.com/",
            facebook: "",
            hh: "https://www.youtube.com/",
            telegram: "",
          },
        },
        {
          image: "2.png",
          name: "Башир Оздоев",
          work: "UX/UI",
          online: false,
          about:
            "Я хочень хороший человек. Без вредных привычек. Не курю, не пью, людей не обижаю. Я хочень хороший человек. Без вредных привычек.Я хочень хороший человек. Без вредных привычек.Я хочень хороший человек. Без вредных привычек.Я хочень хороший человек. Без вредных привычек.Я хочень хороший человек. Без вредных привычек.",
          social: {
            twitter: "https://www.youtube.com/",
            vk: "https://www.youtube.com/",
            facebook: "https://www.youtube.com/",
            hh: "https://www.youtube.com/",
            telegram: "https://www.youtube.com/",
          },
        },
        {
          image: "3.png",
          name: "Дыршткендр Айкен До Ртский",
          work: "UX/UI",
          online: false,
          about:
            "Я хочень хороший человек. Без вредных привычек. Не курю, не пью, людей не обижаю",
          social: {
            twitter: "https://www.youtube.com/",
            vk: "https://www.youtube.com/",
            facebook: "https://www.youtube.com/",
            hh: "",
            telegram: "https://www.youtube.com/",
          },
        },
        {
          image: "4.png",
          name: "Джамбулат Алиев",
          work: "UX/UI",
          online: true,
          about:
            "Я хочень хороший человек. Без вредных привычек. Не курю, не пью, людей не обижаю",
          social: {
            twitter: "",
            vk: "https://www.youtube.com/",
            facebook: "",
            hh: "",
            telegram: "https://www.youtube.com/",
          },
        },
        {
          image: "5.png",
          name: "Вильям Тангиев",
          work: "UX/UI",
          online: false,
          about:
            "Я хочень хороший человек. Без вредных привычек. Не курю, не пью, людей ",
          social: {
            twitter: "https://www.youtube.com/",
            vk: "https://www.youtube.com/",
            facebook: "",
            hh: "https://www.youtube.com/",
            telegram: "https://www.youtube.com/",
          },
        },
        {
          image: "6.png",
          name: "Джони Картоев",
          work: "UX/UI",
          online: true,
          about:
            "Я хочень хороший человек. Без вредных привычек. Не курю, не пью, людей не обижаю",
          social: {
            twitter: "https://www.youtube.com/",
            vk: "https://www.youtube.com/",
            facebook: "https://www.youtube.com/",
            hh: "https://www.youtube.com/",
            telegram: "https://www.youtube.com/",
          },
        },
      ],
    };
  },
};
</script>
