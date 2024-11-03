<template lang="">
  <v-card>
    <v-tabs v-model="tab" align-tabs="center" color="deep-purple-accent-4">
      <v-tab :value="1">Landscape</v-tab>
      <v-tab :value="2">City</v-tab>
      <v-tab :value="3">Abstract</v-tab>
    </v-tabs>

    <v-tabs-window v-model="tab">
      <v-tabs-window-item v-for="n in 3" :key="n" :value="n">
        <v-container fluid>
          <v-row>
            <v-col v-for="i in 6" :key="i" cols="12" md="4">
              <v-img
                :lazy-src="`https://picsum.photos/10/6?image=${i * n * 5 + 10}`"
                :src="`https://picsum.photos/500/300?image=${i * n * 5 + 10}`"
                height="205"
                cover
              ></v-img>
            </v-col>
          </v-row>
        </v-container>
      </v-tabs-window-item>
    </v-tabs-window>
  </v-card>

  <section id="projects" class="project-section">
    <div class="about-top">
      <h1 class="about-title">Projects</h1>
    </div>
    <div class="">
      <div class="carousel" id="carousel">
        <div class="darksoul-carousel">
          <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg1" />
          <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg2" />
          <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg3" />
          <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg4" />

          <div class="apple" @click="apple" id="apple">
            <img
              style="margin-left: 30px; margin-top: 15px"
              width="36"
              height="36"
              src="https://img.icons8.com/external-smashingstocks-glyph-smashing-stocks/66/FFFFFF/external-apple-sports-and-awards-smashingstocks-glyph-smashing-stocks.png"
              alt="external-apple-sports-and-awards-smashingstocks-glyph-smashing-stocks"
            />
            <div class="project-1" id="contentProject">
              <h1>resume</h1>
              <img class="project-1-img" src="../assets/img/project-resume.png" />
              <!-- <p>
                  This project is a Resume Website showcasing my personal information, work
                  experience, skills, and past projects for job applications in web development. It
                  is built using Vue.js, HTML, CSS, and JavaScript, designed to be modern, visually
                  appealing, and fully responsive.
                </p> -->
              <div class="project-1-web"></div>
            </div>
            <img
              src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png"
              id="appleimg"
            />
          </div>

          <div class="lemon" @click="lemon" id="lemon">
            <img
              style="margin-left: 30px; margin-top: 15px"
              width="36"
              height="36"
              src="https://img.icons8.com/glyph-neue/64/1A1A1A/citrus.png"
              alt="citrus"
            />
            <img
              src="https://darksoul-codepen.github.io/Fruits%20Carousel/lemon.png"
              id="lemonimg"
            />
            <h1 id="lemontext">LEMON</h1>
          </div>

          <div class="strawberry" @click="strawberry" id="strawberry">
            <img
              style="margin-left: 30px; margin-top: 15px"
              width="36"
              height="36"
              src="https://img.icons8.com/external-smashingstocks-glyph-smashing-stocks/66/FFFFFF/external-Strawberry-food-smashingstocks-glyph-smashing-stocks.png"
              alt="external-Strawberry-food-smashingstocks-glyph-smashing-stocks"
            />
            <img
              src="https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png"
              id="strawberryimg"
            />
            <h1 id="strawberrytext">BERRY</h1>
          </div>

          <div class="orange" @click="orange" id="orange">
            <img
              style="margin-left: 30px; margin-top: 10px"
              width="36"
              height="36"
              src="https://img.icons8.com/pastel-glyph/64/FFFFFF/citrus-1.png"
              alt="citrus-1"
            />
            <img
              src="https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png"
              id="orangeimg"
            />
            <h1 id="orangetext">ORANGE</h1>
          </div>
        </div>
        <!-- <p class="disclaimer">Designed & Created by <a href="https://darksoul-codepen.github.io/" target="_blank">DarkSoul</a> | Icons by <a href="https://icons8.com/" target="_blank">Icons8</a></p> -->
      </div>
    </div>
  </section>
</template>
<script>
import '../assets/home.css'
export default {
  name: 'HomeView',

  props: {
    isNightMode: {
      type: Boolean,
      required: true
    }
  },
  mounted() {
    this.handleScroll()
    window.addEventListener('scroll', this.handleScroll)
    this.apple()
    this.initializeElements()
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  computed: {
    // orangedivStyle() {
    //   return {
    //   };
    // },
  },
  data() {
    return {
      colors: ['primary', 'secondary', 'yellow darken-2', 'red', 'orange'],
      model: 0,

      // project section
      applediv: null,
      orangediv: null,
      lemondiv: null,
      strawberrydiv: null,
      bodycolor: null,
      appleimg: null,
      orangeimg: null,
      lemonimg: null,
      strawberryimg: null,
      appletext: null,
      orangetext: null,
      lemontext: null,
      strawberrytext: null,
      bgimg1: null,
      bgimg2: null,
      bgimg3: null,
      bgimg4: null,

      selectFruit: '',
      contentProject: null,

      tab: null
    }
  },
  methods: {
    handleScroll() {
      // all section transition
      document.querySelectorAll('section').forEach((section) => {
        const rect = section.getBoundingClientRect()
        if (rect.top < window.innerHeight && rect.bottom > 0) {
          section.classList.add('fade-in')
        } else {
          section.classList.remove('fade-in')
        }
      })

      // home section animation
      const homeSection = document.querySelector('#home')
      const homeTitle = document.querySelector('.home-title')
      const rect = homeSection.getBoundingClientRect()

      if (rect.top < window.innerHeight && rect.bottom > 0) {
        homeTitle.classList.add('tracking-in-expand')
      } else {
        homeTitle.classList.remove('tracking-in-expand')
      }

      // // ตรวจสอบว่า section ใดอยู่ในมุมมองและเพิ่มคลาส 'active' ให้กับ navbar
      // const sections = document.querySelectorAll('section');
      // const navLinks = document.querySelectorAll('.nav-links a');

      // sections.forEach((section, index) => {
      //   const rect = section.getBoundingClientRect();
      //   if (rect.top < window.innerHeight / 2 && rect.bottom >= window.innerHeight / 2) {
      //     navLinks.forEach(link => link.classList.remove('active'));
      //     navLinks[index].classList.add('active');
      //   }
      // });
    },
    initializeElements() {
      this.applediv = document.getElementById('apple')
      this.orangediv = document.getElementById('orange')
      this.lemondiv = document.getElementById('lemon')
      this.strawberrydiv = document.getElementById('strawberry')
      this.bodycolor = document.getElementById('carousel')
      // this.appleimg = document.getElementById("appleimg");
      this.lemonimg = document.getElementById('lemonimg')
      this.orangeimg = document.getElementById('orangeimg')
      this.strawberryimg = document.getElementById('strawberryimg')
      // this.appletext = document.getElementById("appletext");
      this.lemontext = document.getElementById('lemontext')
      this.strawberrytext = document.getElementById('strawberrytext')
      this.orangetext = document.getElementById('orangetext')
      this.bgimg1 = document.getElementById('bgimg1')
      this.bgimg2 = document.getElementById('bgimg2')
      this.bgimg3 = document.getElementById('bgimg3')
      this.bgimg4 = document.getElementById('bgimg4')

      // content in project
      this.contentProject = document.getElementById('contentProject')
    },

    baseElement(color) {
      this.lemondiv.style.width = '100px'
      this.orangediv.style.width = '100px'
      this.applediv.style.width = '100px'
      this.strawberrydiv.style.width = '100px'

      if (this.selectFruit === 'lemon') {
        this.contentProject.style.display = 'none'
        this.lemondiv.style.width = '100%'
        this.bgimg1.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png'
        this.bgimg2.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png'
        this.bgimg3.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png'
        this.bgimg4.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png'
      } else if (this.selectFruit === 'orange') {
        this.orangediv.style.width = '600px'
        bgimg1.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png'
        bgimg2.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png'
        bgimg3.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png'
        bgimg4.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png'
      } else if (this.selectFruit === 'apple') {
        this.contentProject.style.display = 'flex'
        this.applediv.style.width = '600px'
        bgimg1.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png'
        bgimg2.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png'
        bgimg3.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png'
        bgimg4.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png'
      } else if (this.selectFruit === 'strawberry') {
        this.strawberrydiv.style.width = '600px'
        bgimg1.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png'
        bgimg2.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png'
        bgimg3.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png'
        bgimg4.src = 'https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png'
      }

      this.bodycolor.style.backgroundColor = color

      this.orangeimg.style.animation = 'visibility-h 0s linear 0s 1 normal forwards'
      // this.appleimg.style.animation = "visibility-h 0s linear 0s 1 normal forwards";
      this.strawberryimg.style.animation = 'visibility-h 0s linear 0s 1 normal forwards'
      this.lemonimg.style.animation = 'visibility-h 0s linear 0s 1 normal forwards'

      // this.appletext.style.animation = "text-back 1s linear 0s 1 normal forwards";
      this.strawberrytext.style.animation = 'text-back 1s linear 0s 1 normal forwards'
      this.orangetext.style.animation = 'text-back 1s linear 0s 1 normal forwards'
      this.lemontext.style.animation = 'text-back 1s linear 0s 1 normal forwards'

      if (this.selectFruit === 'lemon') {
        lemontext.style.animation = 'text 1s linear 0s 1 normal forwards'
        lemonimg.style.animation = 'down 1s linear 0s 1 normal forwards'
      } else if (this.selectFruit === 'orange') {
        orangeimg.style.animation = 'down 1s linear 0s 1 normal forwards'
        orangetext.style.animation = 'text 1s linear 0s 1 normal forwards'
      } else if (this.selectFruit === 'apple') {
        // appleimg.style.animation = "down 1s linear 0s 1 normal forwards";
        // appletext.style.animation = "text 1s linear 0s 1 normal forwards";
      } else if (this.selectFruit === 'strawberry') {
        strawberryimg.style.animation = 'down 1s linear 0s 1 normal forwards'
        strawberrytext.style.animation = 'text 1s linear 0s 1 normal forwards'
      }
    },

    apple() {
      this.initializeElements()
      this.selectFruit = 'apple'
      this.baseElement('#FF7070')
    },

    lemon() {
      this.initializeElements()
      this.selectFruit = 'lemon'
      this.baseElement('#f7e35b')
    },

    orange() {
      this.initializeElements()
      this.selectFruit = 'orange'
      this.baseElement('#f4a308')
    },

    strawberry() {
      this.initializeElements()
      this.selectFruit = 'strawberry'
      this.baseElement('#FF6286')
    }
  }
}
</script>
<style lang=""></style>
