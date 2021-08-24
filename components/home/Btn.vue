<template>
  <div>
    <v-btn @click="redirect" text>
      {{ btnTitle }}
    </v-btn>
  </div>
</template>

<script>
export default {
  props: {
    btnTitle: String,
  },
  methods: {
    redirect() {
      location.href = '/Menu'; 
    }
  }
};
</script>

<style scoped>
  div {
    text-align: right;
    margin: 10%;
  }
</style>