<template>
  <q-page class="" style="height: 1500px;">
    <AboutSection/>
    <!-- <AboutPage/> -->
    <ProjectPage/>
    <ContactUsForm/>
    <FooterSection/>
  </q-page>
</template>

<script setup>
// import AboutPage from './AboutPage.vue';
import AboutSection from 'src/components/AboutSection.vue';
import AboutPage from './AboutPage.vue';
import ProjectPage from './ProjectPage.vue';
import ContactUsForm from 'src/components/ContactUsForm.vue';
import FooterSection from 'src/components/FooterSection.vue';



defineOptions({
  name: 'IndexPage'
});
</script>
