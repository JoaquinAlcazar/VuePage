<template>
  <div class="panel">
    <viewer v-for="(value, key) in ContentMap" :key="key" class="gamesContent" :title="key" :description="value"
      :image="ImageMap[key]"></viewer>

  </div>
</template>


<script>
import viewer from "@/components/ShowGame.vue"
export default {
  components: {
    viewer
  },
  data() {
    return {
      ContentMap:
      {
        "Dead Cells": "Dead Cells es un videojuego híbrido entre el género de exploración de mazmorras o roguelite, y metroidvania, creando su propio género, “roguevania”, desarrollado por el estudio Motion Twin.1​ El juego fue lanzado para PC, Mac, Linux, Playstation 4, Nintendo Switch y Xbox One,1​ siendo lanzado en la plataforma de Steam el 6 de agosto de 2018, bajo la categoría de juego de acción e indie."
        ,
        "Pokemon XY": "Pokémon X y Pokémon Y, conocidos en Japón como Pocket Monsters X&Y (ポケットモンスター X&Y Poketto Monsutā Ekkusu & Wai?), son dos videojuegos de RPG y aventura, desarrollados por Game Freak y distribuidos por Nintendo para la consola portátil Nintendo 3DS, que fueron lanzados el 12 de octubre de 2013 tanto en Japón como en América, Europa y Australia.2​ Pertenecen a la serie de videojuegos Pokémon, e inauguran la sexta generación de la misma. Fueron anunciados el 8 de enero de 2013 durante el Pokémon Direct por Satoru Iwata, presidente de Nintendo.3​"
      },
      ImageMap: {

        "Dead Cells":
          "/src/components/img/Dead Cells.jpg",
        "Pokemon XY": "/src/components/img/Pokemon.jpg"
      },
      PageState: ["Home", "CRUD", "Api"]
    }
  },
  computed: {

  }
}
</script>

<style scoped>
.panel{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.gamesContent {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;

}
</style>
