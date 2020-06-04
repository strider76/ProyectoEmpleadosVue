<template>
  <div>
    <input type="text" v-model.number="cuenta" />
    <button @click="contar(-1)">Menos</button>
    <button @click="contar(1)">Más</button>

    <p>La cuenta va por {{cuenta}}</p>

    <h3>{{mensaje}}</h3>
  </div>
</template>

<script>
export default {
  name: "Ejemplo",
  props: {
    mensaje: {
      type: String,
      required: false,
      default: "No hay Mensaje"
    }
  },
  data: function() {
    return {
      cuenta: 0
    };
  },
  methods: {
    contar: function(num) {
      this.cuenta += num;
    }
  }
};
</script>

<style>
</style>