<template>
  <div>
    <v-divider></v-divider>
    <div class="text-center my-12">Skills</div>
    <v-row class="">
      <v-col cols="2" class="text-center" v-for="skill in skills" :key="skill.img">
        <v-sheet class="skill-card mb-6 " height="150">
          <v-sheet
            color="transparent skill-sheet"
            class="justify-center ma-2 pa-2 align-self-center"
          >
            <img
              :src="require('../assets/skills/' + skill.img)"
              class="my-3 skill-img"
              contain
              height="60"
              color="white"
            />
          </v-sheet>
        </v-sheet>
      </v-col>
      <!-- <v-col
        md="2"
        sm="5"
        class="text-center"
        v-for="skill in skills"
        :key="skill.img"
      >
        <v-sheet
          class="skill-card justify-center align-center"
          height="150"
          width="150"
        >
          <v-sheet
            color="transparent"
            class="d-flex justify-center align-center mb-1 text-center"
          >
            <v-img
              :src="require('../assets/skills/' + skill.img)"
              class="my-3"
              contain
              height="50"
              color="white"
            />
          </v-sheet>
          <div style="color: white">{{ skill.name }}</div>
        </v-sheet>
      </v-col> -->
    </v-row>
    <!-- <v-row>
            <v-col cols="6" class="d-flex align-items">
              <v-sheet color="transparent" class="d-flex progress-sheet">
                <div>Vue.js</div>
                <div class="progress">
                    <div class="progress-value"></div>
                </div>
              </v-sheet>
            </v-col>
            <v-col cols="6" class="d-flex align-items">
              <v-sheet color="transparent" class="d-flex progress-sheet">
                <div>Vue.js</div>
                <div class="progress">
                    <div class="progress-value"></div>
                </div>
              </v-sheet>
            </v-col>
            <v-col cols="6" class="d-flex align-items">
              <v-sheet color="transparent" class="d-flex progress-sheet">
                <div>Vue.js</div>
                <div class="progress">
                    <div class="progress-value"></div>
                </div>
              </v-sheet>
            </v-col>
        </v-row> -->
  </div>
</template>
<script>
export default {
  setup() {},
  data() {
    return {
      skills: [
        { img: "react.svg", name: "react" },
        { img: "vuetify.svg", name: "vuetify" },
        { img: "vue-js.svg", name: "vue" },
        { img: "python.svg", name: "python" },
        { img: "django.svg", name: "django" },
        { img: "jquery.svg", name: "jquery" },
        { img: "mysql.svg", name: "mysql" },
        { img: "javascript.svg", name: "javascript" },
        { img: "html.svg", name: "html" },
        { img: "css.svg", name: "css" },
        { img: "git.svg", name: "git" },
        { img: "firebase.svg", name: "firebase" },
        { img: "amazon-web-services.svg", name: "aws" },
        { img: "nginx.svg", name: "nginx" },
      ],
    };
  },
};
</script>
<style scoped>
.skill-card >>> .skill-sheet>.skill-img{
  height: 50;
  width: 50;
  cursor: pointer;
  transition: transform .5s;
}
.skill-sheet>>>.skill-img:hover{
  transform: scale(1.5); /* (150% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
}
.skill-card {
  background-color: rgb(67, 70, 86, 0.4);
  border-radius: 5px;
  transition-duration: 1s;
}
.progress {
  background: rgba(255, 255, 255, 0.1);
  justify-content: flex-start;
  border-radius: 100px;
  align-items: center;
  position: relative;
  padding: 0 5px;
  display: flex;
  height: 25px;
  width: 500px;
}
.progress-sheet {
  align-self: center;
  align-items: center;
}
.progress-value {
  animation: load 3s normal forwards;
  box-shadow: 0 10px 30px -10px #fff;
  border-radius: 100px;
  background: #fff;
  height: 20px;
  width: 0;
}

@keyframes load {
  0% {
    width: 0;
  }
  100% {
    width: 68%;
  }
}
/* background: linear-gradient(
    90deg,
    rgba(34, 193, 195, 1) 0%,
    rgba(45, 63, 253, 1) 100%
  ); */
</style>