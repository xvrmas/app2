<template>
  <button v-on:click="alerta1()">Anterior</button>
  <button v-on:click="alerta2()">Següent</button>
  <Escena
    v-bind:text="texte"
    v-on:missatge1="alerta1"
    v-on:missatge2="alerta2"
    v-for="(post, i) in posts"
    :key="i"
    :class="{ active: i === activeItem }"
    :img="post.img"
    :title="post.title"
  >
  </Escena>
</template>

<script>
import Escena from "@/components/Escena.vue";

export default {
  components: { Escena },
  data() {
    return {
      posts: [
        {
          title:
            "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",
          img: "@/assets/1.jpg",
        },
        {
          title:
            "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
          img: "@/assets/2.jpg",
        },
        {
          title: "L'heroi va decidir travessar la porta que el portava a casa",
          img: "@/assets/3.jpg",
        },
        {
          title:
            "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ...",
          img: "@/assets/4.jpg",
        },
      ],
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