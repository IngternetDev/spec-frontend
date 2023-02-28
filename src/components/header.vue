<template>
  <q-header bordered class="header bg-gray-500">
    <div class="header__content">
      <img class="header__logo" src="../assets/header-logo.svg" />
      <img
        @click="darkTheme = !darkTheme"
        class="header__theme"
        :src="
          darkTheme
            ? require('assets/header-moon.svg')
            : require('assets/header-sun.svg')
        "
      />
      <div class="header__profile profile">
        <q-avatar rounded size="35px">
          <img src="../assets/header-ava.png" />
          <q-badge
            floating
            rounded
            :class="isOnline ? 'bg-green' : 'bg-gray-200'"
          />

          <q-menu
            content-class="profile-menu"
            content-style="overflow:inherit"
            :offset="[45, 5]"
          >
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
    </div>
  </q-header>
</template>

<script>
export default {
  data() {
    return {
      isSwitchOn: true,
      darkTheme: true,
      isOnline: true,
    };
  },
};
</script>
