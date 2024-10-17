<template>
  <v-app :class="{ 'night-mode': isNightMode }">
    <!-- <div class="container"> -->
    <div class="top">
      <TopNavBar @toggle-night-mode="toggleNightMode" :is-night-mode="isNightMode" />
    </div>

    <div class="main-content">
      <router-view :is-night-mode="isNightMode" />
    </div>
    <!-- </div> -->
  </v-app>
</template>

<script>
import { defineComponent } from 'vue'
import TopNavBar from '../src/components/TopNavbar.vue'

export default defineComponent({
  components: {
    TopNavBar
  },
  data() {
    return {
      isNightMode: false
    }
  },
  methods: {
    toggleNightMode() {
      this.isNightMode = !this.isNightMode
    }
  }
})
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
  font-family: 'Source Sans 3', sans-serif;
  height: 100%;
  /* scroll-behavior: smooth; */
}
.top {
  margin-bottom: 5.5%;
}
</style>
