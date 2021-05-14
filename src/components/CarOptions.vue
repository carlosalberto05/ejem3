<template>
  <h2>Coche - Options API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>

  <button @click="upPower(50)">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
export default {
  data() {
    return {
      brand: "Seat",
      model: "Leon",
      power: 50,
    };
  },
  methods: {
    upPower(nuevoPower) {
      console.log("Aumentando potencia");
      this.power = this.power + nuevoPower;
    },
    downPower() {
      console.log("Disminuir potencia");
      this.power = this.power - 1;
    },
  },
};
</script>

<style></style>
