<template>
  <v-app
    class="bg-img"
    :class="lightTheme ? 'lgtTheme' : 'darkTheme'"
    id="landing-screen"
  >
  <v-container>
    <!-- <v-sheet :min-height="mdAndUp ? 50 : 0" :rounded="xs"> -->
      <v-app-bar
        v-show="mdAndUp"
        :class="lightTheme ? 'lgtTheme' : 'darkTheme'"
        dark
        color="trasparent"
        elevation="0"
      >
      <v-toolbar-title>NikCoder</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-tabs
          v-model="tab"
          color="blue-accent-3"
          align-tabs="center"
          elevation="0"
          hide-slider
          class="tab-text"
        >
          <v-tab :value="1">Home</v-tab>
          <v-tab :value="2">About</v-tab>
          <v-tab :value="3">Skill</v-tab>
          <v-tab :value="4">Services</v-tab>
          <v-tab :value="5">Contact</v-tab>
        </v-tabs>

        <v-icon class="mx-2" v-if="lightTheme" @click="lightTheme = !lightTheme"
          >mdi-weather-night</v-icon
        >
        <v-icon
          color="yellow accent-4"
          class="mx-2 icon-class"
          v-if="!lightTheme"
          @click="lightTheme = !lightTheme"
          >mdi-white-balance-sunny</v-icon
        >
        <!-- <v-spacer></v-spacer> -->
        <!-- <v-btn elevation="0" class="btn-class">login</v-btn> -->
      </v-app-bar>

      <v-main>
        <router-view />
      </v-main>
    <!-- <MenuBar /> -->
    </v-container>
     <FooterSec />
  </v-app>
</template>

<script>
import { useDisplay } from "vuetify";

// import MenuBar from './components/bottomMenubar'
import FooterSec from './components/footerSec.vue'
export default {
  setup() {
    // Destructure only the keys we want to use
    const { xs, mdAndUp } = useDisplay();
    return { xs, mdAndUp };
  },
  name: "App",
  components: {
    // MenuBar
    FooterSec
  },
  data: () => ({
    tab: null,
    lightTheme: false,
  }),
  methods: {
    themechange() {},
  },
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Poppins&display=swap");
.v-application {
    display: flex;
    background: rgb(var(--v-theme-background));
    color: rgba(0, 0, 0 ,0.87);
}
/* .icon-class{
  box-shadow: 0 0 17px 1px rgba(231,166,26,.6);
} */
.darkTheme {
  background-color: #090b31;
  color: white;
  font-family: Montserrat;
}
.lgtTheme {
  color: #090b31;
  background-color: white;
  font-family: Montserrat;
}
.bg-img {
  background-image: url("@/assets/bg-img.svg");
  transition: background-color 0.5s linear, color 0.5s linear;
  background-size: cover;
  background-repeat: no-repeat;
  /* background-color: rgb(28,24,43)!important; */
}
#landing-screen {
  transition: backgroundImage 0.5s linear;
  -webkit-animation: bg-34d9ae75 0.1s linear;
  animation: bg-34d9ae75 0.1s linear;
}
.btn-class {
  background: linear-gradient(
    to right,
    #9c48d5 0%,
    #9c48d5 5%,
    #2b4eff 64.24%,
    #9c48d5 100%
  );
  background-size: 200% auto;
  border-radius: 40px;
  color: #ffffff;
  padding: 12px 27px;
  transition: all 0.7s ease;
}
.tab-text >>> .v-tab {
  text-transform: capitalize;
  letter-spacing: 0px;
  color: linear-gradient(to top, #1c3881, #090b31);
}
.v-btn--variant-text .v-btn__overlay {
  background: none !important;
}
</style>