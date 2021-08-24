<template>
  <v-carousel cycle
    height="800"
    hide-delimiter-background
    show-arrows-on-hover:show-arrows="false">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: "images/_DSC1758.jpg",
          },
          {
            src: 'images/_DSCsankichi.jpg',
          },
          {
            src: 'images/_DSC1690.jpg',
          },
        ],
      }
    },
  }
</script>
