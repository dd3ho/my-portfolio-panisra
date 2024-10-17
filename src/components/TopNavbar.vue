<template>
  <header class="header" :class="{ 'night-mode': isNightMode }">
    <div class="logo-container">
      <img class="logo-img" src="../assets/img/kitty.png" alt="Kitty" />
      <div class="logo-name" :class="{ 'night-mode': isNightMode }">{{ name_logo }}</div>
    </div>
    <button class="menu-toggle" @click="toggleMenu">☰</button>
    <nav class="nav" :class="{ active: isMenuOpen, 'night-mode': isNightMode }">
      <ul class="nav-links">
        <li><a href="#home" :class="{ 'night-mode': isNightMode }">HOME</a></li>
        <li><a href="#about" :class="{ 'night-mode': isNightMode }">ABOUT</a></li>
        <!-- <li><a href="#tool" :class="{ 'night-mode': isNightMode }">TOOL&SKILL</a></li> -->
        <li><a href="#projects" :class="{ 'night-mode': isNightMode }">PROJECT</a></li>
        <li><a href="#contact" :class="{ 'night-mode': isNightMode }">CONTACT</a></li>
        <li>
          <button class="night-toggle" @click="toggleNightMode">
            <img class="logo-night" :src="nightModeIcon" alt="night" />
          </button>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import nightIcon from '../assets/img/night.png'
import summerIcon from '../assets/img/summer.png'
import '../assets/nav.css'
export default {
  data() {
    return {
      name_logo: '</PANISRA>',
      isMenuOpen: false
    }
  },
  props: {
    isNightMode: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    nightModeIcon() {
      return this.isNightMode ? summerIcon : nightIcon
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    },
    toggleNightMode() {
      this.$emit('toggle-night-mode')
    }
  }
}
</script>

<style></style>
