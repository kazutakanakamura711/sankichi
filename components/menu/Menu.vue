<template>
  <v-row>
    <v-col
      v-for="img in imgs"
      :key="img"
      class="d-flex child-flex"
      cols="12"
      sm="4"
    >
      <v-img :src="img" aspect-ratio="1" class="grey lighten-2">
        <template v-slot:placeholder>
          <v-row class="fill-height ma-0" align="center" justify="center">
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      imgs: [
        "images/_DSC1678.jpg",
        "images/_DSC1698.jpg",
        "images/_DSC1683.jpg",
        "images/_DSC1678.jpg",
        "images/_DSC1698.jpg",
        "images/_DSC1683.jpg",
        "images/_DSC1678.jpg",
        "images/_DSC1698.jpg",
        "images/_DSC1683.jpg",
      ],
    };
  },
};
</script>

<style>
</style>