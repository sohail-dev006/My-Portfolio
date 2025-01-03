<template>
  <q-tabs>
   <q-route-tab v-for="(tab, index) in tabs" :key="index"
      :label="tab.title"
      :to="tab.href"
      class="text-capitalize text-white q-mx-sm"
      exact
    />
  </q-tabs>
</template>
<script setup>
import { ref } from 'vue';
const props = defineProps({
  tabs:{
    type: Array,
  }
}
)

</script>
