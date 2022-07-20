<template>
  <div v-for="(value, i) in posts" :key="i">
    <h4>{{ value.text }}</h4>
  </div>
</template>

<script>
import Boto from "./boto.vue";
export default {
  name: "Escena",
  props: [`posts`],
  // data() {
  //   return {
  //     activeItem: i,
  //   };
  // },
  methods: {
    // selectdItem(i) {
    //   this.activeItem = i;
    // },
  },
  components: { Boto },
};
</script>

<style>
body {
  display: grid;
  align-content: center;
  text-align: center;
}
h4 {
  border: solid;
  border-radius: 40px;
  padding: 10px;
}
</style>