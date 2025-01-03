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
                    <q-btn class="bg-accent q-px-md text-capitalize text-white border-radius-24" dense flat label="Contact" />
                  </div>
                </div>
                <div v-else class="text-right">
                  <q-btn @click="icon1 != icon1" dense flat class="text-white">
                    <q-icon v-if="icon1" name="menu" />
                    <q-icon v-else name="close" />
                    <q-menu class="bg-black text-white" style="border-radius: 14px;"
                    :offset="[0, 6]"
                    >
                    <q-list style="min-width: 300px">
                      <q-item clickable v-close-popup>
                        <div class="q-pa-sm">
                          <li class="q-py-sm">
                            <a href="">home</a>
                          </li>
                          <li class="q-py-sm">
                            <a href="/about">About</a>
                          </li>
                          <li class="q-py-sm">
                            <a href="">Works</a>
                          </li>
                          <li class="q-py-sm">
                            <a href="">Works</a>
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

const icon1 = ref(true);

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
    title: 'FAQ'
  },
])
defineOptions({
  name: 'MainLayout'
})


</script>
