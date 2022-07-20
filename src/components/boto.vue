<template>
  <button @click="$emit(`accio1`,casa)">Anterior</button>
  <button @click="$emit('accio2')">Següent</button>
</template>
<script>
export default {
  props: ["casa"],
  emits: ["accio1", "accio2"],
};
</script>