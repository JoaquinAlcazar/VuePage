<!-- eslint-disable vue/require-v-for-key -->
<template>
  <div>
    <section>
      <article class="table">
        <p class="name">Nombre</p>
        <p class="desc">Description</p>
        <p class="img">fuente de la imagen</p>
        <p class="crud">Borrar</p>
        <p class="crud">Actualizar</p>
      </article>

      <article v-for="objeto in array" class="table">
        <p class="name">{{ objeto.name }}</p>
        <p class="desc">{{ objeto.description }}</p>
        <p class="img">{{ objeto.image }}</p>
        <p class="crud"><button>Borrar</button></p>
        <p class="crud"><button>Actualizar</button></p>
      </article>
    </section>
  </div>

  <tr></tr>

  <p>{{ title }}</p>
  <p>{{ description }}</p>
</template>
<script>
export default {
  name: 'Update-Delete',
  props: {
    array: Array
  },
  methods: {}
}
</script>

<style scoped>
* {
  padding: 0px;
  margin: 0px;
  word-wrap: break-word;
  border: 1px solid black;
}

p{
    text-align: center;
    display: flex;
    justify-content: center; /* Centrar horizontalmente */
    align-items: center;
}

.table {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-left: 5px;
  margin-right: 5px;
  margin-bottom: 1px;
}
.name {
  width: 10%;
  word-break: break-all;

  
}
.desc {
  width: 50%;
  overflow-y: auto;
}
.img {
  width: 20%;
  word-break: break-all;
}
.crud {
  width: 10%;
  word-break: break-all;

}

</style>
