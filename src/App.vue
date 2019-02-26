<template>
  <div id="app">
    <div id="nav" v-if="this.$route.path !== '/'">
      <!-- <router-link to="/">Homes</router-link> |
      <router-link to="/about">About</router-link> -->
      <nav class="utility-nav">
          <router-link to="/" class="utility-nav__item">
              <i class="fas fa-home"></i>
              <span class="utility-nav__text">Home</span>
          </router-link>
          <router-link href="/games" class="utility-nav__item">
              <i class="fas fa-baseball-ball fa-fw"></i>
              <span class="utility-nav__text">Games</span>
          </router-link>
          <router-link href="/divisions" class="utility-nav__item">
              <i class="fas fa-shield-alt fa-fw"></i>
              <span class="utility-nav__text">Divisions</span>
          </router-link>
          <router-link href="/teams" class="utility-nav__item">
              <i class="fas fa-user-shield fa-fw"></i>
              <span class="utility-nav__text">Teams</span>
          </router-link>
          <router-link href="/players" class="utility-nav__item">
              <i class="fas fa-user-circle fa-fw"></i>
              <span class="utility-nav__text">Players</span>
          </router-link>
          <router-link to="/fantasy" class="utility-nav__item">
              <i class="fas fa-star fa-fw"></i>
              <span class="utility-nav__text">fantasy</span>
          </router-link>
      </nav>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
@import "@/assets/styles/styles.scss";
</style>
