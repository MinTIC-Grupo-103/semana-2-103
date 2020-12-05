<template>
  <div class="card h-100">
    <img class="card-img-top" :src="'https://placeimg.com/800/500/'+member.image" alt="" />
        <div>{{member.codigo}}</div>
    <div class="card-body">
      <h4 class="card-title">{{ member.nombre }}</h4>
      <p class="card-text">
        {{member.descripcion}}
      </p>
    </div>

    <span>{{ member.rol}}</span>
    <div class="card-footer">
      <a href="#" class="btn btn-primary">Contactar {{member.nombre.split(" ",1).join()}}!</a>
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