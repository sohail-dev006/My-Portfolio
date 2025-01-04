<template>
    <div class="row justify-center" :class="$q.screen.gt.sm ? 'q-px-xl q-py-md ' : 'q-pa-md'">
      <div class="col-md-11 col-12">
        <div class="row " :class="$q.screen.gt.sm ? '': 'q-col-gutter-y-md'">
          <div class="col-12 bg-black border-radius-12 q-py-md">
            <div class="row q-py-md">
              <div class="col-12">
                <div class="text-center text-white">
                  <h4 class="text-weight-medium">Contact</h4>
                  <h6 class="q-mt-sm">Get in Touch With Me</h6>
                </div>
              </div>
            </div>
            <div class="row q-py-md justify-center">
              <div class="col-10">
                <div class="row wrap q-pb-sm">
                  <div class="col-md-4 col-sm-4 col-12 ">
                    <div class="card q-ma-sm  border-radius-12" :class="$q.screen.gt.sm ? 'q-pa-md':'q-py-md'" style="border: 1px solid rgba(119, 119, 125, .2);">
                      <div class="text-center text-white q-pt-sm">
                        <q-icon class="text-h4 q-py-sm" name="location_on" />
                        <h6 class="q-pb-xs">Location</h6>
                        <p>Swat, Pakistan</p>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-4 col-sm-4 col-12">
                    <div class="card q-ma-sm  border-radius-12" :class="$q.screen.gt.sm ? 'q-pa-md':'q-py-md'" style="border: 1px solid rgba(119, 119, 125, .2);">
                      <div class="text-center text-white q-pt-sm">
                        <q-icon class="text-h4 q-py-sm" name="call" />
                        <h6 class="q-pb-xs">Phone</h6>
                        <p>03498891325</p>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-4 col-sm-4 col-12">
                    <div class="card q-ma-sm  border-radius-12" :class="$q.screen.gt.sm ? 'q-pa-md':'q-py-md'" style="border: 1px solid rgba(119, 119, 125, .2);">
                      <div class="text-center text-white q-pt-sm">
                        <q-icon class="text-h4 q-py-sm" name="mail" />
                        <h6 class="q-pb-xs">Email</h6>
                        <p>sohaildev006@gmail.com</p>
                      </div>
                    </div>
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
import { ref } from 'vue';

</script>



<style>

</style>
