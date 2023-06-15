<template>
  <HelloWorld />
  <AboutUs/>
  <SkillSet />
  <ExperienceHere />
  <ContactUs />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import HelloWorld from '../components/HelloWorld.vue';
import AboutUs from '../components/AboutUs.vue';
import SkillSet from '../components/SkilllSet.vue';
import ExperienceHere from '../components/experienceHere.vue';
import ContactUs from '@/components/contactUs.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    HelloWorld,
    AboutUs,
    SkillSet,
    ExperienceHere,
    ContactUs,
  },
});
</script>
