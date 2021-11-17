<template>
  <v-carousel
    cycle
    height="100vh"
    hide-delimiter-background
    show-arrows-on-hover:show-arrows="false"
  >
    <v-carousel-item
      v-for="(item, i) in slideImgs"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  props: {
    slideImgs: Array,
  },
};
</script>
<style lang="scss" scoped>
</style>
