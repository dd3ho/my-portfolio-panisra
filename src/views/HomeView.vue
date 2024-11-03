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
        <div class="wave-section">
          <div class="wave wave1"></div>
          <div class="wave wave2"></div>
          <div class="wave wave3"></div>
          <div class="wave wave4"></div>
        </div>
      </div>
      <div class="home-right">
        <img class="img-dev" src="../assets/img/profile.png" alt="developer" />
        <h3 class="name-home">Panisra Wongbubpa</h3>
        <h4 class="email-home">panisraparn@gmail.com</h4>
        <div class="social-links">
          <!-- GitHub -->
          <a href="https://github.com/dd3ho" target="_blank" class="github-link">
            <img src="../assets/img/github-mark.png" alt="GitHub" class="github-image" />
          </a>

          <!-- LinkedIn -->
          <a href="https://linkedin.com/in/yourusername" target="_blank">
            <!-- <img src="linkedin-logo.png" alt="LinkedIn" /> -->
          </a>

          <!-- Email -->
          <a href="mailto:panpanisra@gmail.com">
            <img src="../assets/img/email-logo.png" alt="Email" />
          </a>
        </div>
        <button class="home-btn">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
          contact
        </button>
      </div>
    </section>

    <!-- about section -->
    <section id="about" class="about-section">
      <div class="about-top">
        <h1 class="about-title">ABOUT ME</h1>
      </div>
      <div class="about-bottom">
        <div class="about-left">
          <!-- <h1>That's me!</h1> -->
          <!-- <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
            <path
              fill="#ff5500"
              fill-opacity="1"
              d="M0,288L48,272C96,256,192,224,288,197.3C384,171,480,149,576,165.3C672,181,768,235,864,250.7C960,267,1056,245,1152,250.7C1248,256,1344,288,1392,304L1440,320L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
            ></path>
          </svg> -->
          <!-- <div class="wave-section">
            <div class="wave wave1"></div>
            <div class="wave wave2"></div>
            <div class="wave wave3"></div>
            <div class="wave wave4"></div>
          </div> -->

          <!-- CAT WALK -->
          <!-- <div id="marco">
            <div id="cielo"></div>
            <div id="gato"></div>
            <div id="muro"></div>
            <div id="edificios"></div>
          </div> -->

          <!-- TOOL -->
          <div class="tool">
            <div class="tag">UI Design</div>
            <div class="tag">python</div>
            <div class="tag">java</div>
            <div class="tag">javascript</div>
            <div class="tag">HTML/CSS</div>
            <div class="tag">Vue.js</div>
            <div class="tag">Django</div>
            <div class="tag">React</div>
            <div class="tag">Vuetify</div>
            <div class="tag">Leadership</div>
            <!-- <div class="tag">Sketch</div> -->
            <!-- <div class="tag">Adobe Suite</div> -->
          </div>
        </div>

        <div class="about-right">
          <div class="x">
            <div class="x-left"></div>
            <div class="x-right"></div>
            <div class="x-right"></div>
          </div>
          <h2>
            I'm a recent graduate with a degree in Computer Science, eager to start my career in
            software development. I am passionate about learning new technologies and solving
            challenging problems.
          </h2>
        </div>
      </div>

      <div class="education-section">
        <div class="exp-title">
          <h2>Education</h2>
        </div>
        <div class="exp-container">
          <div class="exp-card">
            <div class="exp-year">
              <span>2020 - 2024</span>
            </div>
            <div class="exp-content">
              <h2>Bachelor of Computer Science</h2>
              <p>KASETSART UNIVERSITY (BANGKHEN)</p>
            </div>
            <div class="exp-description">
              <p>
                Engaged in coursework related to computer science, including software development,
                algorithms, and data structures. Participated in hackathons and collaborated on
                projects.
              </p>
              <p>GPA: 2.70</p>
            </div>
          </div>
        </div>
      </div>

      <div class="about-experience">
        <div class="exp-title">
          <h2>Experience</h2>
        </div>
        <div class="exp-container">
          <!-- Software Developer Intern Experience Card -->
          <div class="exp-card">
            <div class="exp-year">
              <span>2023</span>
            </div>
            <div class="exp-content">
              <h2>Software Developer Intern</h2>
              <p>Trinity Roots Co., Ltd.</p>
              <p>Jun 1 - Oct 31, 2023</p>
            </div>
            <div class="exp-description">
              <p>
                Developed and maintained systems using Django and Vue.js, implemented features,
                performed manual testing, and collaborated with the team to resolve issues. Gained
                full-stack development skills and real-world experience.
              </p>
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
      <div class="card">
        <v-card>
          <!-- Tabs -->
          <v-tabs v-model="tab" bg-color="pink-accent-1" key="tabs">
            <v-tab :key="1" value="one">E-commerce</v-tab>
            <v-tab :key="2" value="two">Loan System Management</v-tab>
            <v-tab :key="3" value="three">POS (Point of Sale) KAfee Cafe</v-tab>
            <v-tab :key="4" value="fourth">KU Leave Management System</v-tab>
            <v-tab :key="5" value="fifth">My Portfolio</v-tab>
          </v-tabs>

          <!-- Window to display tab content -->
          <v-card-text>
            <v-window v-model="tab" key="window">
              <!-- E-commerce Project Description -->
              <v-window-item :key="1" value="one">
                <div class="project-content text-center">
                  <!-- Project Image -->
                  <v-img
                    src="../assets/img/project-e-commerce.png"
                    max-width="600"
                    class="project-image mx-auto mb-6"
                  />

                  <!-- Project Description -->
                  <p class="project-description mt-4">
                    The online marketplace system consists of three main features: User for browsing
                    and purchasing products, Seller for managing inventory, and Admin for managing
                    user accounts and overseeing the system. Each role is designed to simplify
                    processes and ensure smooth transactions.
                  </p>

                  <!-- Project Links -->
                  <div class="link-container mt-4">
                    <a
                      href="https://github.com/dd3ho/E-commerce-JavaFX"
                      target="_blank"
                      class="project-link ml-4"
                    >
                      View on GitHub
                    </a>
                  </div>
                </div>
              </v-window-item>

              <!-- Loan System Management Description -->
              <v-window-item :key="2" value="two">
                <div class="project-content text-center">
                  <!-- Project Image -->
                  <v-img
                    src="../assets/img/project-banking.png"
                    max-width="600"
                    class="project-image mx-auto mb-6"
                  />

                  <!-- Project Description -->
                  <p class="project-description mt-4">
                    This is an application pertaining to the management of loan systems within a
                    bank, designed for bank employees. It features various functions such as
                    customer registration system, document recording system, contract recording
                    system, invoicing system, and others.
                  </p>

                  <!-- Project Links -->
                  <div class="link-container mt-4">
                    <a
                      href="https://github.com/dd3ho/Loan_System_Management_JavaFX"
                      target="_blank"
                      class="project-link ml-4"
                    >
                      View on GitHub
                    </a>
                  </div>
                </div>
              </v-window-item>

              <!-- POS System Description -->
              <v-window-item :key="3" value="three">
                <div class="project-content text-center">
                  <!-- Project Image -->
                  <v-img
                    src="../assets/img/project-pos.png"
                    max-width="600"
                    class="project-image mx-auto mb-6"
                  />

                  <!-- Project Description -->
                  <p class="project-description mt-4">
                    The project is designed to enhance the management and efficiency of coffee shop
                    operations. It provides a web application for streamlined staff management, menu
                    updates, and sales promotions. The system also includes features for managing
                    loyalty programs and coupons to improve customer service and operational
                    efficiency.
                  </p>

                  <!-- Project Links -->
                  <div class="link-container mt-4">
                    <a
                      href="https://github.com/dd3ho/POS_Kafee_Cafe"
                      target="_blank"
                      class="project-link ml-4"
                    >
                      View on GitHub
                    </a>
                  </div>
                </div>
              </v-window-item>

              <!-- KU Leave Management System Description -->
              <v-window-item :key="4" value="fourth">
                <div class="project-content text-center">
                  <!-- Project Image -->
                  <v-img
                    src="../assets/img/project-leave.png"
                    max-width="600"
                    class="project-image mx-auto mb-6"
                  />

                  <!-- Project Description -->
                  <p class="project-description mt-4">
                    The KU Leave Management System is a web application designed to streamline the
                    process of submitting and approving leave requests for students. It allows
                    students to easily request various types of leave, while faculty can efficiently
                    review and manage these requests, track their status, and maintain leave
                    history.
                  </p>

                  <!-- Project Links -->
                  <div class="link-container mt-4">
                    <a
                      href="https://github.com/dd3ho/Leave_Management_System_Banckend"
                      target="_blank"
                      class="project-link ml-4"
                    >
                      View Backend on GitHub
                    </a>
                    <a
                      href="https://github.com/PsYcHo6908/Leave_Management_Forntend"
                      target="_blank"
                      class="project-link ml-4"
                    >
                      View Frontend on GitHub
                    </a>
                  </div>
                </div>
              </v-window-item>

              <!-- Portfolio Project Description -->
              <v-window-item :key="5" value="fifth">
                <div class="project-content text-center">
                  <!-- Project Image -->
                  <v-img
                    src="../assets/img/project-resume.png"
                    max-width="600"
                    class="project-image mx-auto mb-6"
                  />

                  <!-- Project Description -->
                  <p class="project-description mt-4">
                    This portfolio project showcases my work and skills, utilizing technologies such
                    as Vue.js and Vuetify to create a responsive and modern design. It includes
                    various sections that provide information about my projects, skills, and how to
                    contact me.
                  </p>

                  <!-- Project Links -->
                  <div class="link-container mt-4">
                    <a href="https://your-portfolio-link.com" target="_blank" class="project-link">
                      View Project
                    </a>
                    <a
                      href="https://github.com/dd3ho/my-portfolio-panisra"
                      target="_blank"
                      class="project-link ml-4"
                    >
                      View on GitHub
                    </a>
                  </div>
                </div>
              </v-window-item>
            </v-window>
          </v-card-text>
        </v-card>
      </div>
    </section>

    <section id="contact" class="contact-section">
      <div class="container">
        <h1>Contact Me</h1>
        <p>
          Feel free to contact me by submitting the form below and I will get back to you as soon as
          possible.
        </p>
        <form @submit.prevent="sendEmail" class="contact-form">
          <div class="form-group">
            <label for="name">Name</label>
            <input
              type="text"
              v-model="name"
              id="name"
              name="name"
              required
              placeholder="Enter name"
            />
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input
              type="email"
              v-model="email"
              id="email"
              name="email"
              required
              placeholder="Enter email"
            />
          </div>
          <div class="form-group">
            <label for="message">Message</label>
            <textarea
              v-model="message"
              id="message"
              name="message"
              rows="4"
              required
              placeholder="Write your Message"
            ></textarea>
          </div>
          <button type="submit" class="submit-btn">Send Message</button>
        </form>
      </div>
    </section>
  </div>
</template>

<script>
import emailjs from 'emailjs-com'
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
    // this.apple()
    // this.initializeElements()
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
      tab: 'one',

      // contact section
      name: '',
      email: '',
      message: ''
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
    sendEmail() {
      const serviceID = 'service_gkz77nn'
      const templateID = 'template_bkztpsv'
      const userID = 'AcylwjHvB9gnzPiER'

      emailjs
        .send(
          serviceID,
          templateID,
          {
            from_name: this.name,
            reply_to: this.email,
            message: this.message
          },
          userID
        )
        .then(() => {
          alert('Email sent successfully!')
          this.name = ''
          this.email = ''
          this.message = ''
          console.log('Email sent successfully!', response.status, response.text)
        })
        .catch((err) => {
          alert('Failed to send email. Please try again.')
          console.error(err)
        })
    }
  }
}
</script>
