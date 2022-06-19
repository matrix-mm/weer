<template>
  <v-content>
    <div class="staticHero">
      <v-img src="../assets/images/img13.jpg">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">About Us</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container>
        <p>Weer Designed and Weer Made.
Work in progress for an installation which is a result of collision and collaboration of three different fields of creativity at the Building Bridges Exhibition.
Come experience our work which will be open to public starting from the 18th of July.</p>
      </v-container>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">Our Teams</h2>
        <v-row>
          <v-col v-for="item in items" :key="item.id" class="d-flex child-flex" cols="12" sm="4">
            <v-card flat tile class="mx-auto">
              <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2"></v-img>
              <v-card-text class="text--primary text-center">
                <div class="title">{{ item.name }}</div>
                <p>{{ item.title }}</p>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-content>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/images/team1.jpg"),
          name: 'Peter Smith',
          title: 'Director'
        },
        {
          id: 2,
          src: require("../assets/images/team2.jpg"),
          name: 'Roy Perry',
          title: 'Photographer'
        },
        {
          id: 3,
          src: require("../assets/images/team3.jpg"),
          name: 'Lisa White',
          title: 'Freelancer'
        }
      ]
    };
  }
};
</script>