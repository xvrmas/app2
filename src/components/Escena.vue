<template>
  <div>
    <h4>{{ title }}</h4>
  </div>
</template>

<script>
export default {
  name: "Escena",
  props: ["title", "img"],
  methods: {},
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