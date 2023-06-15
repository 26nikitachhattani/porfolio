<template>
  <div class="my-3">
    <v-divider></v-divider>
    <div class="text-center my-12">Skills</div>
    <v-row class="justify-space-around">
      <v-col class="text-center" cols="3">
          <v-tabs v-model="tab" hide-slider >
        <v-tab>education</v-tab>
        <v-tab>work</v-tab>
      </v-tabs>
      </v-col>
    </v-row>
    <v-row class="justify-space-around">
      <v-col cols="7">
       <div width="300px" class="justify-center">
       
       </div>
        <v-window v-model="tab">
      <v-window-item>
            <v-timeline align="start" line-color="#6666cc" line-thickness="1">
              <v-timeline-item
                v-for="(year, i) in years"
                :key="i"
                :dot-color="year.color"
                size="15px"
              >
                <div>
                  <h4
                    :class="`mt-1 headline font-weight-light mb-4 text-${year.color}`"
                  >
                    Lorem ipsum
                  </h4>
                  <div
                    :class="`mt-n1 headline font-weight-bold text-${year.color}`"
                    v-text="year.year"
                  ></div>
                  <div class="font-weight-light">
                    Lorem ipsum dolor sit amet, no nam oblique veritus. Commune
                  </div>
                </div>
              </v-timeline-item>
            </v-timeline>
      </v-window-item>
      <v-window-item>
            <v-timeline align="start" line-color="#6666cc">
      <v-timeline-item
        v-for="(year, i) in years"
        :key="i"
        :dot-color="year.color"
        size="15px"
      >
        <!-- <template v-slot:opposite>
          <div
            :class="`pt-1 headline font-weight-bold text-${year.color}`"
            v-text="year.year"
          ></div>
        </template> -->
        <div>
          <h4
            :class="`my-0 headline font-weight-light mb-4 text-${year.color}`"
          >
            Lorem ipsum
          </h4>
           <div
            :class="`pt-n1 headline font-weight-bold text-${year.color}`"
            v-text="year.year"
          ></div>
        </div>
      </v-timeline-item>
    </v-timeline>
      </v-window-item>
        </v-window>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data: () => ({
    tab: null,
    years: [
      {
        color: "#6666cc",
        year: "1960",
      },
      {
        color: "#6666cc",
        year: "1980",
      },
      {
        color: "amber",
        year: "1990",
      },
      {
        color: "orange",
        year: "2000",
      },
    ],
  }),
};
</script>