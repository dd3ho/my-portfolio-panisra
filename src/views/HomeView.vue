<template>
  <div class="container" :class="{ 'night-mode': isNightMode }">
    <section id="home" class="home-section">
      <div class="home-left">
        <h1 class="home-title">Hello, I am Panisra Wongbubpa</h1>
        <div class="home-description">
          <p>
            A web developer excited to start my new career, I created this website to help you get
            to know me better. Here, you can explore some of the projects I’ve worked on, which
            showcase my skills and approach to web development.
          </p>
        </div>
      </div>
      <div class="home-right">
        <img class="img-dev" src="../assets/img/developer.png" alt="developer" />
      </div>
    </section>

    <!-- about section -->
    <section id="about" class="about-section">
      <div class="about-top">
        <h1 class="about-title">ABOUT ME</h1>
      </div>
      <div class="about-bottom">

        <div class="about-left">
          <img src="../assets/img/profile.png" alt="Profile Picture" class="profile-picture"/>
          <div class="about-introduce">
            <h3>Welcome</h3>
            <p>Hello! I'm a recent graduate with a degree in Computer Science, eager to start my career in software development. I am passionate about learning new technologies and solving challenging problems.</p>
          </div>
          <div class="education">
            <h3>Education</h3>
            <ul>
              <li>Bachelor’s in Computer Science from Kasetsart University (Bangkhen)</li>
              <li>GPA: 2.70</li>
            </ul>
          </div>
          <div class="skill">
            <h3>Skill</h3>
            <div class="skill-box">
              <div class="skill-item">JavaScript</div>
              <div class="skill-item">HTML</div>
              <div class="skill-item">CSS</div>
              <div class="skill-item">PYTHON</div>
              <div class="skill-item">DJANGO</div>
              <div class="skill-item">VUE JS</div>
              <div class="skill-item">REACT</div>
              <div class="skill-item">SQL</div>
            </div>
          </div>

          <div class="skill">
            <h3>Tool</h3>
            <div class="skill-box">
              <div class="skill-item">Git</div>
              <div class="skill-item">Postman</div>
              <div class="skill-item">VS Code</div>
            </div>
          </div>
        </div>



        <div class="about-right">
          <h2 class="about-header2">Timeline</h2>
          <div class="timeline">
            <div class="timeline-item">
              <div class="timeline-content">
                <h3>2020-2024 New graduate</h3>
                <h4>Kasetsart University (Bangkhen)</h4>
                <h5>Major: Computer Science</h5>
                <h5>GPA: 2.70</h5>
              </div>
            </div>
            <div class="timeline-item">
              <div class="timeline-content">
                <h3>Jun 1 - Oct 31, 2023</h3>
                <h4>Internships Software Developer</h4>
                <h5>@Trinity Roots Co., Ltd.</h5>
                <p>
                  During my internship at Trinity Roots Co., Ltd., I worked as a Software Developer using Django and Vue.js.
                  My main responsibilities included:
                  <ul>
                    <li>Developing and maintaining both customer-facing and admin dashboards using Django for the backend and Vue.js for the frontend.</li>
                    <li>Implementing and validating various features and functionalities as per the project requirements.</li>
                    <li>Conducting manual testing to ensure the quality and functionality of the applications.</li>
                    <li>Collaborating with team members to troubleshoot and resolve issues.</li>
                    <li>Documenting the testing procedures and results to support future development and debugging efforts.</li>
                  </ul>
                  This experience allowed me to enhance my skills in full-stack development and gain hands-on experience with both Django and Vue.js in a real-world environment.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

  <!-- projects section -->
  <section id="projects" class="project-section">
    <div class="about-top">
      <h1 class="about-title">Projects</h1>
    </div>
    <div class="">
    <div class="carousel" id="carousel">
      <div class="darksoul-carousel">
        <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg1"/>
        <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg2"/>
        <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg3"/>
        <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="bgimg4"/>
        
        <div class="apple" @click="apple"  id="apple">
            <img style="margin-left: 30px; margin-top: 15px;" width="36" height="36" src="https://img.icons8.com/external-smashingstocks-glyph-smashing-stocks/66/FFFFFF/external-apple-sports-and-awards-smashingstocks-glyph-smashing-stocks.png" alt="external-apple-sports-and-awards-smashingstocks-glyph-smashing-stocks"/>
            <div class="project-1" id="contentProject">
              <h1>resume</h1>
              <img class="project-1-img" src="../assets/img/project-resume.png"/>
              <p>this is resume website to represent how am i</p>
              <div class="project-1-web"></div>
            </div>
           <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png" id="appleimg"/>
        </div>

        <div class="lemon" @click="lemon" id="lemon">
            <img style="margin-left: 30px; margin-top: 15px;" width="36" height="36" src="https://img.icons8.com/glyph-neue/64/1A1A1A/citrus.png" alt="citrus"/>
            <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/lemon.png" id="lemonimg"/>
            <h1 id="lemontext">LEMON</h1>
        </div>

        <div class="strawberry" @click="strawberry" id="strawberry">
            <img style="margin-left: 30px; margin-top: 15px;" width="36" height="36" src="https://img.icons8.com/external-smashingstocks-glyph-smashing-stocks/66/FFFFFF/external-Strawberry-food-smashingstocks-glyph-smashing-stocks.png" alt="external-Strawberry-food-smashingstocks-glyph-smashing-stocks"/>
            <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png" id="strawberryimg"/>
            <h1 id="strawberrytext">BERRY</h1>
        </div>

        <div class="orange" @click="orange" id="orange">
            <img style="margin-left: 30px; margin-top: 10px;" width="36" height="36" src="https://img.icons8.com/pastel-glyph/64/FFFFFF/citrus-1.png" alt="citrus-1"/>
            <img src="https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png" id="orangeimg"/>
            <h1 id="orangetext">ORANGE</h1>
        </div>

    </div>
    <!-- <p class="disclaimer">Designed & Created by <a href="https://darksoul-codepen.github.io/" target="_blank">DarkSoul</a> | Icons by <a href="https://icons8.com/" target="_blank">Icons8</a></p> -->
    </div>

  </div>
  </section>


    <section id="contact" class="contact-section">
      <div class="container">
        <h1>Contact Me</h1>
        <p>Feel free to Contact me by submitting the form below and I will get back to you as soon as possible.</p>
        <form class="contact-form">
          <div class="form-group">
            <label for="name">Name</label>
            <input type="text" id="name" name="name" required placeholder="Enter name">
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" name="email" required placeholder="Enter email">
          </div>
          <div class="form-group">
            <label for="message">Message</label>
            <textarea id="message" name="message" rows="4" required placeholder="Write your Message"></textarea>
          </div>
          <button type="submit" class="submit-btn">Send Message</button>
        </form>
      </div>
    </section>


    
  </div>
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
    this.apple();
    this.initializeElements();
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
      colors: [
          'primary',
          'secondary',
          'yellow darken-2',
          'red',
          'orange',
        ],
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

        selectFruit: "",
        contentProject: null
    };
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
      this.applediv = document.getElementById("apple");
      this.orangediv = document.getElementById("orange");
      this.lemondiv = document.getElementById("lemon");
      this.strawberrydiv = document.getElementById("strawberry");
      this.bodycolor = document.getElementById("carousel");
      // this.appleimg = document.getElementById("appleimg");
      this.lemonimg = document.getElementById("lemonimg");
      this.orangeimg = document.getElementById("orangeimg");
      this.strawberryimg = document.getElementById("strawberryimg");
      // this.appletext = document.getElementById("appletext");
      this.lemontext = document.getElementById("lemontext");
      this.strawberrytext = document.getElementById("strawberrytext");
      this.orangetext = document.getElementById("orangetext");
      this.bgimg1 = document.getElementById("bgimg1");
      this.bgimg2 = document.getElementById("bgimg2");
      this.bgimg3 = document.getElementById("bgimg3");
      this.bgimg4 = document.getElementById("bgimg4");

      // content in project
      this.contentProject = document.getElementById("contentProject");
},

baseElement(color) {

  this.lemondiv.style.width = "100px";
  this.orangediv.style.width = "100px";
  this.applediv.style.width = "100px";
  this.strawberrydiv.style.width = "100px";

  if (this.selectFruit === "lemon") {
    this.contentProject.style.display = "none";
    this.lemondiv.style.width = "100%";
    this.bgimg1.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png";
    this.bgimg2.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png";
    this.bgimg3.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png";
    this.bgimg4.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/lemonbg.png";

  } else if (this.selectFruit === "orange") {
    this.orangediv.style.width = "600px";
    bgimg1.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png";
    bgimg2.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png";
    bgimg3.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png";
    bgimg4.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/orange.png";

  } else if (this.selectFruit === "apple") {
    this.contentProject.style.display = "flex";
    this.applediv.style.width = "600px";
    bgimg1.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png";
    bgimg2.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png";
    bgimg3.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png";
    bgimg4.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/apple.png";



  } else if (this.selectFruit === "strawberry") {
    this.strawberrydiv.style.width = "600px";
    bgimg1.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png";
    bgimg2.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png";
    bgimg3.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png";
    bgimg4.src = "https://darksoul-codepen.github.io/Fruits%20Carousel/strawberry.png";
  }

  this.bodycolor.style.backgroundColor = color;

  this.orangeimg.style.animation = "visibility-h 0s linear 0s 1 normal forwards";
  // this.appleimg.style.animation = "visibility-h 0s linear 0s 1 normal forwards";
  this.strawberryimg.style.animation = "visibility-h 0s linear 0s 1 normal forwards";
  this.lemonimg.style.animation = "visibility-h 0s linear 0s 1 normal forwards";

  // this.appletext.style.animation = "text-back 1s linear 0s 1 normal forwards";
  this.strawberrytext.style.animation = "text-back 1s linear 0s 1 normal forwards";
  this.orangetext.style.animation = "text-back 1s linear 0s 1 normal forwards";
  this.lemontext.style.animation = "text-back 1s linear 0s 1 normal forwards";

  if (this.selectFruit === "lemon") {
    lemontext.style.animation = "text 1s linear 0s 1 normal forwards";
    lemonimg.style.animation = "down 1s linear 0s 1 normal forwards";

  } else if (this.selectFruit === "orange") {
    orangeimg.style.animation = "down 1s linear 0s 1 normal forwards";
    orangetext.style.animation = "text 1s linear 0s 1 normal forwards";

  } else if (this.selectFruit === "apple") {
    // appleimg.style.animation = "down 1s linear 0s 1 normal forwards";
    // appletext.style.animation = "text 1s linear 0s 1 normal forwards";



  } else if (this.selectFruit === "strawberry") {
    strawberryimg.style.animation = "down 1s linear 0s 1 normal forwards";
    strawberrytext.style.animation = "text 1s linear 0s 1 normal forwards";
    
  }

},

apple() {
  this.initializeElements();
  this.selectFruit = "apple"
  this.baseElement("#FF7070");
},

lemon() {
  this.initializeElements();
  this.selectFruit = "lemon"
  this.baseElement("#f7e35b");
},

orange() {
  this.initializeElements();
  this.selectFruit = "orange"
  this.baseElement("#f4a308");
},

strawberry() {
  this.initializeElements();
  this.selectFruit = "strawberry"
  this.baseElement("#FF6286");
}




  }
}
</script>
