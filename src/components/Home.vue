<template>
  <Escena :posts="posts"></Escena>
</template>

<script>
import Escena from "@/components/Escena.vue";
export default {
  components: { Escena },

  data() {
    return {
      posts: [
        {id:1,
          text: `El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial`,
        },
        {id:2,
          text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
        },
        {id:3,
          text: "L'heroi va decidir travessar la porta que el portava a casa",
        },
        {id:4,
          text: "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ...",
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