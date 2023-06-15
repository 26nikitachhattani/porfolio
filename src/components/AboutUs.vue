<template>
  <div class="my-14">
    <h1 class="mt-4 text-center">About Us</h1>
    <div class="sub-title text-center mb-6">My Intoduction</div>
    <v-row>
      <v-col cols="6">
        <div style="border-radius: 10px">
          <v-img
            :src="require('../assets/me.jpg')"
            class="my-3"
            contain
            height="300"
          />
        </div>
      </v-col>
      <v-col cols="5">
        <div>
          I'm Nikita Chhattani, a dedicated software developer engineer
          specializing in frontend development. With 3+ years of experience, I
          excel in both frontend and backend development, particularly with
          Python and Django. My passion lies in transforming ideas into
          functional software solutions.
          <br />
          <br />
          I love learning new technologies and constantly experimenting with
          different languages and tools. Whether it's designing intuitive
          interfaces or building robust backend architectures, I'm committed to
          delivering exceptional results. Skills: HTML, CSS, JavaScript, React,
          Vue.js, Python, Django, RESTful APIs, PostgreSQL, MySQL, MongoDB, Git,
          Problem Solving.
          <br />
          <br />
          If you're looking for a skilled software developer engineer to bring
          your ideas to life, let's collaborate and create something amazing
          together. Contact me to discuss your project further.
        </div>
      </v-col>
    </v-row>
  </div>
</template>
<style scoped>
.sub-title {
  color: #7e7e7e;
  font-weight: 500;
}
</style>