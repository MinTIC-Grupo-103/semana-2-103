<template>
  <div class="card h-100">
    <!-- <img class="card-img-top" src="http://placehold.it/500x500" alt="" /> -->
    <img class="card-img-top" :src="'https://placeimg.com/800/500/'+member.image" alt="" />

    <!-- src="https://placeimg.com/800/350/"+ -->
    <!-- <img class="card-img-top" :src="member.imagen" alt="alt" /> -->
    <div class="card-body">
      <h4 class="card-title">{{ member.nombre }}</h4>
      <p class="card-text">
        {{member.descripcion}}
      </p>
    </div>
    <span>{{ member.rol}}</span>
    <div class="card-footer">
      <a href="#" class="btn btn-primary">Saber mas!</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped>
</style>