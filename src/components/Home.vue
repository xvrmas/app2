<template>
  <Escena :posts="posts"></Escena>
</template>

<script>
import Escena from "@/components/Escena.vue";
export default {
  components: { Escena },
  data() {
    return {
      posts:
     { text: `El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial`},
      
    };
  },
  methods: {
    alerta1() {
      alert("Hola");
    },
    alerta2() {
      alert("Adios");
    },
  },
};
</script>


<style>
button {
  padding: 20px;
  width: 50%;
  font-size: 25px;
}
</style>