<template>

  <div v-if="condition">
    <div
      v-for="(value, i) in llista"
      :key="i"
      :class="{ active: i === seleccionat }"
      :imatge="value.img"
    >
    
      <h4>{{ value.text }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "Escena",
  props: [`llista`, "seleccionat", "condition"],
  data() {
    return {
      active: null,
    };
  },
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
  background-color: rgb(255, 255, 255);
  border-radius: 40px;
  padding: 10px;
}

.active > h4 {
  background-color: rgb(244, 190, 184);
}
</style>