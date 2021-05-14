<template>
  <h2>Coche - Composition</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPower(300)">Disminuir</button>
</template>

<script>
export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    const power = 40;

    const upPower = () => {
      console.log("Aumentar potencia...");
    };

    const downPower = (newPower) => {
      console.log("Bajar potencia..." + newPower);
    };

    return {
      brand,
      model,
      power,
      upPower,
      downPower,
    };
  },
};
</script>

<style></style>
