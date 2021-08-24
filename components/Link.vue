<template>
<div>
  <nuxt-link 
  tag="div"
  class="link"
  :to="linkDestination">{{titleName}}</nuxt-link>
</div>

</template>
<script>
export default {
  props: {
    linkDestination: null,
    titleName: String,
  }
}

</script>

<style >
  .link {
    letter-spacing: 0.5em;
    text-align: right;
    margin: 10%;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.3s 0s ease;
  }
  .link:hover {
    color: rgb(194, 20, 20);
  }
</style>