<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="" style="background-color: black;" elevated>
      <div class="row justify-center" :class="$q.screen.gt.sm ? 'q-px-xl q-py-md ' : 'q-pa-sm'">
        <div class="col-md-11 col-12">
          <div class="row">
            <div class="col-12">
              <div class="row justify-between items-center" :class="$q.screen.gt.sm ? 'q-pa-xs' : 'q-pa-sm'">
                <div class="col-md-2">
                  <div class="">
                    <q-img width="50px" class="bg-transparent" height="40px" src="src/assets/Logo.png" />
                  </div>
                </div>
                <div v-if="$q.screen.gt.sm" class="col-md-8">
                  <NavTabs :tabs="tabs"/>
                </div>
                <div v-if="$q.screen.gt.sm" class="col-md-2">
                  <div class="text-right">
                    <q-btn class="bg-accent q-px-md text-capitalize text-white border-radius-24" dense flat label="Hire Me" />
                  </div>
                </div>
                <div v-else class="text-right">
                  <q-btn @click="icon1 != icon1" dense flat class="text-white">
                    <q-icon v-if="icon1" name="close" />
                    <q-icon v-else name="menu" />
                    <q-menu class="bg-black text-white" style="border-radius: 14px;"
                    :offset="[5, 6]"
                    >
                    <q-list style="min-width: 300px">
                      <q-item clickable v-close-popup>
                        <div class="q-pa-sm">
                          <li class="q-py-sm" style="list-style: none;">
                            <a href="" class="text-decore text-white text-h6">Home</a>
                          </li>
                          <li class="q-py-sm" style="list-style: none;">
                            <a href="/about" class="text-decore text-white text-h6">About</a>
                          </li>
                          <li class="q-py-sm" style="list-style: none;">
                            <a href="" class="text-decore text-white text-h6">Project</a>
                          </li>
                          <li class="q-py-sm" style="list-style: none;">
                            <a href="" class="text-decore text-white text-h6">Contact</a>
                          </li>
                          <li class="q-py-sm" style="list-style: none;">
                            <q-btn class="bg-accent q-px-md text-capitalize text-white border-radius-24" dense flat label="Hire Me" />
                          </li>
                        </div>
                      </q-item>
                    </q-list>
                   </q-menu>
                  </q-btn>
                </div>
               </div>
            </div>
          </div>
        </div>
        </div>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import NavTabs from 'src/components/NavTabs.vue';

const icon1 = ref(false);

let tabs = ref([
  {
    title: 'Home',
    href: '/'
  },
  {
    title: 'About',
    href: '/about'
  },
  {
    title: 'Project',
    href: '/project'
  },
  {
    title: 'Contact'
  },
])
defineOptions({
  name: 'MainLayout'
})


</script>
