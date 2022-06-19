<template>
  <div class="block latestPostBlock">
    <v-container>
      <h2 class="text-center">Latest Post</h2>
      <v-row>
        <v-col v-for="item in items" :key="item.id" cols="12" md="4">
          <v-card outlined class="mx-auto">
            <v-img
              class="white--text align-end"
              height="200px"
              :src="item.src"
            >
              <v-card-title>{{ item.title }}</v-card-title>
            </v-img>
            <v-card-subtitle class="pb-0">{{ item.subtitle }}</v-card-subtitle>
            <v-card-text class="text--primary">
              <div>{{ item.description }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn color="primary" text>More</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "LatestPost",
  data: () => ({
    show: false,
    items: [
      {
        id: 1,
        title: "Penthouse (Yangon)",
        subtitle: "penthouse project",
        description: "This penthouse project, located in North Dagon Township, is created with the aim of providing a 'safe space', an escape from the tediousness and stresses of conventional lifestyle. The design approach is to accomodate a compact, simple and minimalistic space within confined site with limitations.",
        src: require("../assets/images/img-carousel5.jpg")
      },
      {
        id: 2,
        title: "Biodiversity Education Center - Putao",
        subtitle: "2,000 miles of wonder",
        description: "Located in northern Myanmar, the small town of Putao is surrounded by ice-capped mountains and presents a unique vegetation, including rare orchids, as well as endemic birds and animals. This diverse ecosystem is celebrated in the new Biodiversity Education Center Putao, which opened its doors to the public in December 2019.",
        src: require("../assets/images/img1.1.jpg")
      },
      {
        id: 3,
        title: "Elephant Museum",
        subtitle: "3,000 miles of wonder",
        description: "This design is an entry proposal for the competition for the first ever elephant museum in Myanmar and it was selected as the winner of the competition in October 2018.The main idea of the design is based upon the coherent flow of sectional zones for different categories and suggested circulation of guests around it.",
        src: require("../assets/images/img3.1.jpg")
      }
    ]
  })
};
</script>