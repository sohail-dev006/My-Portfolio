<template>
  <div class="row justify-center" :class="$q.screen.gt.sm ? 'q-px-xl q-py-md ' : 'q-pa-md'">
    <div class="col-md-11 col-12">
      <div class="row " :class="$q.screen.gt.sm ? 'q-col-gutter-lg': 'q-col-gutter-y-md'">
        <div class="col-md-4 col-12">
          <div class="bg-black border-radius-12 text-center">
            <div class="q-pt-lg">
              <q-avatar class="text-center bg-white" size="196px">
                <img src="src/assets/My_profile_672x694.jpeg" />
              </q-avatar>
            </div>
            <div class="text-white">
              <h4 class="q-my-none q-pt-sm text-weight-medium" :class="$q.screen.gt.sm ? 'q-pb-sm' : ''">Sohail Ahmed</h4>
              <p class="text-h6 q-mb-none" :class="$q.screen.lt.md ? 'q-px-xs': ($q.screen.gt.md ? 'q-px-xl' : 'q-px-lg')">I am a Frontend Developer based in Swat, Pakistan</p>
            </div>
            <q-item class="text-white row q-pb-md justify-center" :class="$q.screen.gt.md ? 'q-mx-auto' :''">
              <q-btn href="https://github.com/sohail-dev006" flat dense class=" text-h4" :class="$q.screen.gt.md ? 'q-px-md' :''">
                <i class="fa-brands fa-github"></i>
              </q-btn>
              <q-btn href="https://www.linkedin.com/in/sohail-dev006/" flat dense class=" text-h4" :class="$q.screen.gt.md ? 'q-px-md' :''">
                <i class="fa-brands fa-linkedin"></i>
              </q-btn>
              <q-btn href="https://www.instagram.com/zangi__006?igsh=dm9xNnNxZnQ5cHMz" flat dense class=" text-h4" :class="$q.screen.gt.md ? 'q-px-md' :''">
                <i class="fa-brands fa-square-instagram"></i>
              </q-btn>
              <q-btn href="https://www.facebook.com/Sohail.ZanGi" flat dense class=" text-h4" :class="$q.screen.gt.md ? 'q-px-md' :''">
                <i class="fa-brands fa-facebook"></i>
              </q-btn>
            </q-item>
          </div>
        </div>
        <div class="col-md-8 col-12">
          <div class="bg-black border-radius-12">
            <div class="text-white q-px-md q-py-sm">
              <h4 class="q-my-md q-pl-sm text-bold">Hello There!</h4>
              <p class="text-h5 q-pl-sm ">I'm Sohail Ahmed, a passionate Frontend Software Developer 🚀 with a focus on building web and mobile applications using HTML, CSS, Bootstrap, JavaScript, Quasar Framework, Vue.js, and other exciting libraries and frameworks.</p>
              <div class="q-pl-sm ">
                <li class="">Ready to Take on New Challenges</li>
              </div>
              <div class=" q-py-md q-pl-sm">
                <q-btn flat dense  class="text-capitalize q-px-md q-mt-xs bg-accent">Download CV</q-btn>
              </div>
            </div>
          </div>
          <div class="bg-black border-radius-12 q-mt-md">
            <div class="text-white q-pt-sm">
              <div class="q-pl-md q-ml-xs text-weight-medium" :class="$q.screen.gt.sm ? 'q-py-md text-h4': 'q-py-sm text-h5'">What I Do</div>
              <div class="scroll-container q-pb-md">
               <div class="scroll">
                 <div class="scroll-content" v-for="(item, index) in items" :key="index">
                   <q-item class="scroll-item" :class="$q.screen.gt.md ? 'q-py-lg': ''">
                    <div class="skill">{{ item.name }}</div>
                   </q-item>
                 </div>
               </div>
             </div>
            </div>
          </div>
        </div>
      </div>
      <EducationSection/>
    </div>
  </div>
</template>

<script setup>
import EducationSection from './EducationSection.vue';

const items = [
  {
    icon: 'src/assets/html.png',
    name: 'HTML'
  },
  {
    icon: 'src/assets/css.png',
    name: 'CSS'
  },
  {
    icon: 'src/assets/javascript.webp',
    name: 'JavaScript'
  },
  {
    icon: 'src/assets/bootstrap.png',
    name: 'Bootstrap 5'
  },
  {
    icon: 'src/assets/vue3.png',
    name: 'Vue.js'
  },
  {
    icon: 'src/assets/quasar.png',
    name: 'Quasar Framework'
  },
]
</script>

<style scoped>
.scroll-container {
  overflow: hidden; /* Hide any overflowing text */
  white-space: nowrap; /* Prevent line breaks */
  width: 100%; /* Full width */
  position: relative; /* Positioning context */

}

.scroll {
  display: inline-flex; /* Keep items in a single line */
  animation: scroll-left 20s linear infinite; /* Animation for scrolling */
}

.scroll-content {
  display: inline-block; /* Keep items inline */
  margin-right: 20px; /* Space between items */
}
.skill {
    background-color: transparent;
    border: 1px solid #333;
    color: #fff;
    padding: 7px 20px;
    border-radius: 5px;
    font-size: 18px;
    font-family: Poppins, sans-serif;
    text-transform: uppercase;
    white-space: nowrap;
    transition: background-color .3s ease;
}
@keyframes scroll-left {
  from {
    transform: translateX(0); /* Start position */
  }
  to {
    transform: translateX(-40%); /* Move to half of the total width of the scroll */
  }
}
</style>

