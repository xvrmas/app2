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
  <div v-if="!condition">
  <h3>Benviguts a la web de formació</h3><br>
    <button @click="mostrar">{{ 'Iniciar' }}</button>
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
        },
        {
          text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
        },
        { text: "L'heroi va decidir travessar la porta que el portava a casa" },
        {
          text: "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ...",
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
</style>