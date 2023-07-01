<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">We are Zosia and Alena</h1>
              <span class="text-grey">Web Designers & Developers</span><br />

              <v-btn tile dark class="text-blue mt-8" variant="outlined" href="https://www.google.com/intl/pl/gmail/about/">
                Contact us
                
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
              class="mt-16"
            >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="i.1.png" contain max-height="500"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="i.2.png" max-height="300" class=""></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16" style="font-size:24px;">About Us</h5>
              <div style="width: 120px">
                <v-slider
                  v-model="slider2"
                  color="blue"
                  label="track-color"
                ></v-slider>
              </div>
              <h4 class="mt-n4">We are Creative Web Designers</h4>
              <h4 class="">And Developers</h4>
              <p class="text-grey">
                Our combined expertise in design and development allows us to create websites that not only look great 
                but also deliver a seamless user experience.
                Whether you need a simple portfolio website, an e-commerce platform, 
                or a complex web application, we have the skills and knowledge to bring your vision to life.
              </p>
              <br />
              <p class="text-grey">
                We work closely with our clients throughout the entire design and development process to ensure 
                that we deliver a product that meets all of their requirements and exceeds their expectations. 
                We believe that communication is key,
                so we make sure to keep our clients informed and involved every step of the way.
              </p>
              <v-btn tile dark color="blue" class="mt-4" @click="downloadPDF">
                Download Resume
              </v-btn>

            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What We Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider
            v-model="slider2"
            color="blue"
            label="track-color"
          ></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                  icon="fas fa-laptop"
                  color="#2288f5"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                   We create the visual layout,  
                    <br />user interface, 
                  <br /> and overall look of a website.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-mobile-alt"
                  color="#2288f5"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  We create user interface   <br />and user experience
                  <br />for a mobile application.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fa-solid fa-bag-shopping"
                  color="#2288f5"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Product Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  We create the physical    <br /> and digital form
                  <br /> of a product.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#2288f5" class="mr-2" @click="filterProjects('all')">All</v-btn>
          <v-btn class="mr-2" variant="tonal" @click="filterProjects('web')">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal" @click="filterProjects('front')">Front Design</v-btn>
          <v-btn class="mr-2" variant="tonal" @click="filterProjects('product')">Product Design</v-btn>
        </div>
        <!-- <div v-for="project in filteredItems" :key="project.img">
          
        </div> -->
      </v-col>
      
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img :src="item.img" height="225px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#2288f5" class="mt-4" @click="loadMore">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="i.10.jpg" height="200px" cover></v-img>

                <v-card-title> Reliable </v-card-title>

                <v-card-subtitle>
                  By ZOLENA
                </v-card-subtitle>
                <v-card-text>
                  You can trust that we will be there every step 
                  of the way to provide support and answer any questions you may have. 
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="i.11.jpg" height="200px" cover></v-img>

                <v-card-title> Best quality </v-card-title>

                <v-card-subtitle>
                  By ZOLENA 
                </v-card-subtitle>
                <v-card-text>
                  From the initial consultation to the final product delivery, 
                  we are committed to providing you with the highest level of service.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="i.12.jpg" height="200px" cover></v-img>

                <v-card-title> Customization </v-card-title>

                <v-card-subtitle>
                  By ZOLENA
                </v-card-subtitle>
                <v-card-text>
                  We take the time to understand your business needs and work with you 
                  to create a website that is tailored to your specific requirements. 
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire us for your awesome project</h1>
              <p class="text-grey">
                We look forward to working with you to create a website that showcases your brand and helps you achieve your goals.
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#2288f5" class="mt-15">Hire Us</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">Gdańsk, Poland </span
              ><br />
              <v-btn
                icon="fas fa-phone-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">736-482-937 </span> <br />
              <span class="text-caption">938-472-635 </span> <br />
              <v-btn
                icon="fas fa-envelope"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">zofiaassg@gmail.com </span> <br />
              <span class="text-caption">alena.mi@gmail.com </span> <br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption"
              >If you need a website designed or developed, feel free to send us a message!
               We would be happy to discuss your project and provide you with a quote. Contact us today to get started!</span
            >
            <form action="https://getform.io/f/d15a9529-660c-4b7e-a281-d9dda634f056" method="POST" enctype="multipart/form-data">
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                type="text"
                  label="Name"
                  persistent-hint
                  variant="outlined"
                  name="name"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  type="email"
                  label="Email"
                  persistent-hint
                  variant="outlined"
                  name="email"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Message"
              persistent-hint
              variant="outlined"
              name="message"
            ></v-textarea>
            <v-btn color="#2288f5" class="mt-2" type="submit">Submit Now</v-btn>
          </form>
          </v-col>
        </v-row>
        
      </v-col>
    </v-container>
    <FooterView />
    <v-btn fab bottom right class="scroll-top-button" @click="scrollToTop">
      UP!
    </v-btn>
  </v-app>
</template>



<script>
import { defineComponent } from "vue";
import NavBar from "../components/NavBar.vue";
import FooterView from "../components/FooterView.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    NavBar,
    FooterView
  },
  setup() {
    
    return {
      
      slider2: 50,

      items: [
        {
          img: "i.3.png",
        },
        {
          img: "i.4.png",
        },
        {
          img: "i.5.png",
        },
        {
          img: "i.6.jpg",
        },
        {
          img: "i.9.jpg",
        },
        {
          img: "i.8.jpg",
        },
      ],
    };
  },
//   setup() {
    
    
//     const items = [
//       {
//         img: "i.3.png",
//       },
//       {
//         img: "i.4.png",
//       },
//       {
//         img: "i.5.png",
//       },
//       {
//         img: "i.6.jpg",
//       },
//       {
//         img: "i.9.jpg",
//       },
//       {
//         img: "i.8.jpg",
//       },
//       {
//         img: "i.13.png",
//       },
//       {
//         img: "i.14.png",
//       },
//       {
//         img: "i.15.png",
//       },
//     ];
//     const displayedItems = ref(items.slice(0, 3));

// const loadMore = () => {
//   const startIndex = displayedItems.value.length;
//   const endIndex = startIndex + 3;
//   displayedItems.value = displayedItems.value.concat(items.slice(startIndex, endIndex));
// };

// return {
//   slider2: 50,
//   displayedItems,
//   loadMore,
// };
//   },
  // data() {
  //   return {
  //     selectedCategory: "all",
  //     slider2: 50,
  //     items: [
  //       {
  //         img: "i.3.png",
  //         category: "web",
  //       },
  //       {
  //         img: "i.4.png",
  //         category: "front",
  //       },
  //       {
  //         img: "i.5.png",
  //         category: "web",
  //       },
  //       {
  //         img: "i.6.jpg",
  //         category: "product",
  //       },
  //       {
  //         img: "i.9.jpg",
  //         category: "front",
  //       },
  //       {
  //         img: "i.8.jpg",
  //         category: "web",
  //       },
  //     ],
  //   };
  // },
  // computed: {
  //   filteredItems() {
  //     if (this.selectedCategory === "all") {
  //       return this.items; // Отобразить все проекты
  //     } else {
  //       return this.items.filter(item => item.category === this.selectedCategory); // Фильтровать проекты по категории
  //     }
  //   },
  // },
  methods: {
    // filterProjects(category) {
    //   this.selectedCategory = category;
    // },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
    downloadPDF() {
      const fileUrl = "portfolio-master/public/resume.pdf"; // Замените на путь к вашему файлу PDF
      const link = document.createElement("a");
      link.href = fileUrl;
      link.setAttribute("download", "resume.pdf");
      link.style.display = "none";
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    },
  },
  
});

</script>

<style scoped>

.scroll-top-button {
  position: fixed;
  right: 24px;
  bottom: 24px;
  border-radius: 25%;
  background-color: rgba(0, 0, 0, 0.1);
  color: white;
  transition: background-color 0.3s;
}

.scroll-top-button:hover {
  background-color: rgba(0, 0, 0, 0.7);
}

.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover {
  padding: 0 200px;
}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}

</style>
