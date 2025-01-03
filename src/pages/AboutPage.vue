<template>
  <div class="row justify-center" id="/about" :class="$q.screen.gt.sm ? 'q-px-xl q-py-md ' : 'q-pa-md'">
    <div class="col-md-11 col-12">
      <div class="row " :class="$q.screen.gt.sm ? 'q-col-gutter-lg': 'q-col-gutter-y-md'">
        <div class="col-md-4 col-12">
          <div class="bg-black border-radius-12 text-center">
            <div class="q-pt-lg">
              <q-avatar class="text-center bg-white q-pt-md " size="196px">
                <!-- <img src="src/assets/f7228cab16fd92b349118b06e935964b.jpg" /> -->
              </q-avatar>
            </div>
            <div class="text-white">
              <h6 class="q-my-none text-h3" :class="$q.screen.gt.sm ? 'q-py-md' : ''">Name</h6>
              <p class="text-h6" :class="$q.screen.lt.md ? 'q-px-xs': ($q.screen.gt.md ? 'q-px-xl' : 'q-px-lg')">I am a Frontend Developer based in Swat, Pakistan</p>
            </div>
            <q-item class="text-white row q-pb-xl q-px-xl " :class="$q.screen.gt.xs ? 'q-mx-lg' :''">
              <q-item-section class="q-px-none text-h4">
                <i class="fa-brands fa-github"></i>
              </q-item-section>
              <q-item-section class="q-px-none text-h4">
                <i class="fa-brands fa-linkedin"></i>
              </q-item-section>
              <q-item-section class="q-px-none text-h4">
                <i class="fa-brands fa-square-instagram"></i>
              </q-item-section>
              <q-item-section class="q-px-none text-h4">
                <i class="fa-brands fa-facebook"></i>
              </q-item-section>
            </q-item>
          </div>
        </div>
        <div class="col-md-8 col-12">
          <div class="bg-black border-radius-12">
            <div class="text-white q-px-md q-py-sm">
              <h4 class="q-my-md q-pl-sm text-bold">Hello There!</h4>
              <p class="text-h5 q-pl-sm ">I'm Salman Shahid, a passionate Frontend Software Developer 🚀 with a focus on building web-development using JavaScript, React.js, and other exciting libraries and frameworks.</p>
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
              <div class="q-pl-md q-ml-xs" :class="$q.screen.gt.sm ? 'q-py-md text-h4': 'q-py-sm text-h5'">What I Do</div>
              <div class="scroll-container q-pb-md">
               <div class="scroll">
                 <div class="scroll-content" v-for="(item, index) in items" :key="index">
                   <q-item class="scroll-item">
                    <div class="skill">{{ item.name }}</div>
                   </q-item>
                 </div>
               </div>
             </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row q-mt-md">
        <div class="col-12">
          <div class="bg-black border-radius-12 text-white">
            <div class="q-pa-lg">
              <h4 class="q-mb-xs" :class="$q.screen.gt.xs ? '' : 'text-h6'">Education</h4>
              <div class="row items-center q-pt-sm">
                <div class="q-pr-md">
                  <q-icon class="text-h3" name="school" />
                </div>
                <div class="">
                  <p class="q-my-none">2022 - 2024</p>
                  <h5 class="q-my-none">Higher Secondary Education</h5>
                  <p class="q-my-none">Ncr-Cet College</p>
                </div>
              </div>
              <div class="row items-center q-pt-md">
                <div class="q-pr-md">
                  <q-icon class="text-h3" name="school" />
                </div>
                <div class="">
                  <p class="q-my-none">2022 - 2024</p>
                  <h5 class="q-my-none">Higher Secondary Education</h5>
                  <p class="q-my-none">Ncr-Cet College</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
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
    padding: 10px 20px;
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

