<template>
  <v-container>
    <v-footer padless>
      <v-card flat class="text-center">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
        <v-card-text
          class="pt-0"
        >Weer Designed and Weer Made.
Work in progress for an installation which is a result of collision and collaboration of three different fields of creativity at the Building Bridges Exhibition.
Come experience our work which will be open to public starting from the 18th of July.</v-card-text>
        <v-divider></v-divider>
        <v-card-text>
          {{ new Date().getFullYear() }} —
          <strong>© 2022 All Rights Reserved . WeeR | Architectural Designer</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-container>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    icons: [
      "fab fa-facebook",
      "fab fa-twitter",
      "fab fa-google-plus",
      "fab fa-linkedin",
      "fab fa-instagram"
    ]
  })
};
</script>