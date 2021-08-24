<template>
  
  <v-img
    lazy-src=""
    max-height="650"
    max-width="1550"
    :src="contentTitleImg"
  >
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="text-h4 font-weight-thin mb-4 ">{{ contentTitleH1 }}</h1>
        <h4 class="subheading">{{ contentTitleH4 }}</h4>
      </v-col>
    </v-row>
  </v-img>
  
</template>
<script>
export default {
  props: {
    contentTitleImg: String,
    contentTitleH1: String,
    contentTitleH4: String,
  }
};
</script>

<style>
  h1 {
    color: aliceblue;
  }
  h4 {
    color: rgba(235, 0, 0, 0.945);
  }
</style>