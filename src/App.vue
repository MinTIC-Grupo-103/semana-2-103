<template>
  <div id="app">
    <!-- Carousel -->
    <section-carousel></section-carousel>
    <div class="container">
      <!-- Noticias -->
      <!-- TODO: Crearcomponente con API de noticias -->
      <!-- Lista de miembros -->
      <div class="pb-5">
        <div class="row text-center">
          <div
            class="col-lg-3 col-md-6 mb-4"
            v-for="(item, index) of team"
            :key="index"
          >
            <team-card v-bind:member="item"></team-card>
          </div>
        </div>
      </div>
      <!-- /.row -->
    </div>
    <!-- Footer -->
    <page-footer>
      <h1>{{ title }}</h1></page-footer
    >
  </div>
</template>

<script>
import PageFooter from "./components/PageFooter.vue";
import SectionCarousel from "./components/SectionCarousel.vue";
import TeamCard from "./components/TeamCard.vue";

export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    SectionCarousel,
  },
  data() {
    TeamCard;
    return {
      title: "vivo dentro de vue",
      team: [
        {
          codigo: 1,
          nombre: "Fabian Gamboa Gomez",
          descripcion:
            "Gestionar el proceso Scrum y ayudar a eliminar impedimentos que puedan afectar a la entrega del producto.",
          rol: "Scrum Master",
          image: "perro",
        },
        {
          codigo: 2,
          nombre: "Santiago rendon Valencia",
          descripcion:
            "Encargado de optimizar y maximizar el valor del producto, siendo la persona encargada de gestionar el flujo de valor del producto a través del Product Backlog. ",
          rol: "Product Owner",
          image: "gato",
        },
        {
          codigo: 3,
          nombre: "Edith Andrea Rincon Perez",
          descripcion: "Se encarga de gestionar y asegurar que el proceso Scrum se lleva a cabo correctamente, así como de facilitar la ejecución del proceso y sus mecánicas. ",
          rol: "Equipo de desarrollo",
          image: "mariposa",
        },
        {
          codigo: 4,
          nombre: "Cindy Peralta Palmeira",
          descripcion: "Indica la necesidad de ayudar a eliminar progresiva y constantemente impedimentos que van surgiendo en la organización y que afectan a su capacidad para entregar valor.",
          rol: "Equipo de desarrollo",
          image: "leon",
        },
      ],
    };
  },
};
</script>
