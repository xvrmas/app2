<template>
  <Boto
    @accio1="selectedItem1"
    @accio2="selectedItem2"
    :condition="condition"
  ></Boto>
  <Escena
    :llista="posts"
    :seleccionat="currentSentence"
    :condition="condition"
  ></Escena>
  <div class="careta" v-if="!condition">
    <h3>Benviguts a la web de formació</h3>
    <br />
    <button class="boto-inici" @click="mostrar">{{ "Iniciar" }}</button>
  </div>
</template>

<script>
import Escena from "@/components/Escena.vue";
import Boto from "@/components/Boto";
export default {
  components: { Escena, Boto },

  data() {
    return {
      posts: [
        {
          text: `El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial`,
          img: { src: require("@/assets/1.jpg") },
        },
        {
          text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
          img: "@/assets/2.jpg",
        },
        {
          text: "L'heroi va decidir travessar la porta que el portava a casa",
          img: "@/assets/3.jpg",
        },
        {
          text: "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ...",
          img: "@/assets/4.jpg",
        },
      ],
      currentSentence: 0,
      condition: false,
    };
  },
  methods: {
    mostrar() {
      this.condition = true;
    },
    selectedItem1() {
      this.currentSentence--;
    },
    selectedItem2() {
      this.currentSentence++;
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
.careta {
  padding: 200px;
}
.boto-inici {
  background-color:salmon;
  color:white;
  border: 0;
  border-radius: 50px;
  width: auto;
}
.boto-inici:hover {
  background-color:rgb(244, 60, 39);
}
</style>