<template>
  <q-header bordered class="header bg-gray-500">
    <div class="header__content">
      <img class="header__logo" src="../assets/header/logo.svg" />
      <div class="header__profile profile">
        <q-avatar size="35px">
          <div class="profile__img">
            <img src="../assets/header/ava.png" />
            <div class="profile__status-circle"></div>
          </div>

          <q-menu content-class="profile-menu" :offset="[45, 5]">
            <ul class="profile-menu__list">
              <li class="profile-menu__item" @click="isSwitchOn = !isSwitchOn">
                <a href="#" class="profile-menu__link"> Доступен</a>
                <div
                  class="profile-menu__switch"
                  :class="{ 'switch-on': isSwitchOn }"
                ></div>
              </li>

              <li class="profile-menu__item">
                <a href="#" class="profile-menu__link">Профиль</a>
              </li>
              <li class="profile-menu__item">
                <a href="#" class="profile-menu__link">Настройки</a>
              </li>
              <li class="profile-menu__item">
                <a href="#" class="profile-menu__link">Помощь</a>
              </li>
            </ul>
          </q-menu>
        </q-avatar>
      </div>
      <img
        v-if="darkTheme"
        @click="darkTheme = !darkTheme"
        class="header__theme"
        src="../assets/header/sun.svg"
      />
      <img
        v-else
        @click="darkTheme = !darkTheme"
        class="header__theme"
        src="../assets/header/moon.svg"
      />
    </div>
  </q-header>
</template>

<script>
export default {
  data() {
    return {
      isSwitchOn: true,
      darkTheme: true,
      isOnline: false,
    };
  },
  methods: {},
};
</script>

<style></style>
