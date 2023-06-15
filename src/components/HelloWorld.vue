<template>
  <v-container>
    <v-row class="justify-space-around row-style">
      <v-col cols="12" md="5" class="d-flex mb-4 text-left col-style">
        <div class="mx-3 mt-3">
          <div class="my-2">
            <v-icon color="deep-purple">mdi-instagram</v-icon>
          </div>
          <div class="my-2">
            <v-icon color="deep-purple">mdi-git</v-icon>
          </div>
          <div class="my-2">
            <v-icon color="deep-purple">mdi-linkedin</v-icon>
          </div>
        </div>
        <div>
          <h1>Hey I am <span class="wave">👋</span></h1>
          <h1 class="font-weight-bold mb-3" style="font-size: 40px">
            
            Nikita Chhattani
          </h1>
          <div class="sub-heading">Web Developer</div>
          <p class="mt-3 subheading font-weight-regular">
            I have a passion for building intuitive, user-friendly interfaces that provide an enjoyable and seamless user experience.
          </p>
          <v-btn class="mt-4 btn-class" height="60px" >Contact me</v-btn>
        </div>
        
      </v-col>
      <v-col cols="12" md="3" class="text-center col-style">
        <div class="image-border-class" height="400" width="400">
           <v-img
          :src="require('../assets/front.svg')"
          class="my-3"
          contain
          height="300"
        />
        </div>
        <!-- <v-img
          :src="require('../assets/front.svg')"
          class="my-3"
          contain
          height="300"
        /> -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    }),
};
</script>
<style scoped>
.row-style {
  height: 450px;
}
.col-style {
  align-self: center;
}
.image-border-class{
  box-shadow: 0 0 17px 1px rgba(231,166,26,.6);
  border-radius: 50%;
  border: 30px solid #ffc107;
  padding: 40px;
}
.sub-heading {
  color: #7e7e7e;
  font-weight: 500;
  font-size: 25px;
}
.wave {
  animation-name: wave-animation;  /* Refers to the name of your @keyframes element below */
  animation-duration: 2.5s;        /* Change to speed up or slow down */
  animation-iteration-count: infinite;  /* Never stop waving :) */
  transform-origin: 70% 70%;       /* Pivot around the bottom-left palm */
  display: inline-block;
}
@keyframes wave-animation {
    0% { transform: rotate( 0.0deg) }
   10% { transform: rotate(14.0deg) }  /* The following five values can be played with to make the waving more or less extreme */
   20% { transform: rotate(-8.0deg) }
   30% { transform: rotate(14.0deg) }
   40% { transform: rotate(-4.0deg) }
   50% { transform: rotate(10.0deg) }
   60% { transform: rotate( 0.0deg) }  /* Reset for the last half to pause */
  100% { transform: rotate( 0.0deg) }
}
.btn-class {
  background: linear-gradient(
    to right,
    #9c48d5 0%,
    #9c48d5 5%,
    #2b4eff 64.24%,
    #9c48d5 100%
  );
  letter-spacing: 0;
  text-transform: capitalize;
  background-size: 200% auto;
  border-radius: 10px;
  color: #ffffff;
  padding: 7px 27px;
  transition: all 0.7s ease;
}
</style>