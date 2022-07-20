<template>
  <button @click="$emit(`accio1`,caseta)">Anterior</button>
  <button @click="$emit('accio2')">Següent</button>
</template>
<script>
export default {
  name:"Boto",
  emits: ["accio1", "accio2"],
  props:['caseta']
};
</script>