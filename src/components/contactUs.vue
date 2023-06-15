<template>
  <div class="my-5">
    <h1 class="text-center mt-7">Contact Us</h1>
    <div class="text-center">Get in Touch</div>
    <v-card color="transparent">
      <v-row class="my-3 justify-space-around">
        <v-col cols="3" class="justify-center">
          <div class="contact-div my-3" v-for="con in contacts" :key="con">
            <div class="">
              <v-icon small color="#6666cc" class="mt-1 mx-2">{{
                con.icon
              }}</v-icon>
              <div class="contact-title">
                {{ con.title }}
              </div>
            </div>
            <div class="contact-subtitle">{{ con.contact }}</div>
          </div>
        </v-col>
        <v-col cols="5">
          <v-card
            class="py-4"
            color="transparent"
            elevation="3"
            style="border: 1px solid #fff"
          >
            <v-card-text>
              <v-row>
                <v-col cols="6">
                  <div>Name</div>
                  <v-text-field
                    class="my-1"
                    label="Name"
                    persistent-hint
                    variant="outlined"
                  ></v-text-field>
                </v-col>
                <v-col cols="6">
                  <div>Email</div>
                  <v-text-field
                    class="my-1"
                    label="Name"
                    persistent-hint
                    variant="outlined"
                  ></v-text-field>
                </v-col>
                <v-col cols="12" class="my-0 py-0">
                  <div>Projects</div>
                  <v-text-field
                    class="my-1"
                    label="Name"
                    persistent-hint
                    variant="outlined"
                  ></v-text-field>
                
              <div>Name</div>
              <v-textarea
        
                label="One row"
                auto-grow
                variant="outlined"
                rows="1"
                row-height="15"
              ></v-textarea></v-col>
              </v-row>
              
            </v-card-text>
            <v-card-actions class="text-center">
                <v-btn class="btn-class" height="60px" elevation="0">Send Message</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    contacts: [
      {
        title: "Email",
        contact: "26niktachhattani@gmail.com",
        icon: "mdi-email-outline",
      },
      { title: "Call on", contact: "7999493840", icon: "mdi-phone-outline" },
      {
        title: "Location",
        contact: "Raipur Chhattisgarh",
        icon: "mdi-map-marker-outline",
      },
    ],
  }),
};
</script>
<style scoped>
.contact-title {
  font-size: 1.5rem;
}
.contact-subtitle {
  color: #7e7e7e;
  font-weight: 500;
  font-size: 15px;
}
.inputField {
  border-radius: 6px;
  font-family: Source Sans Pro;
  font-size: 17px;
  font-weight: 400;
  color: rgba(51, 51, 51, 0.74);
  height: 60px;
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