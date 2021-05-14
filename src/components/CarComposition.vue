<template>
  <h2>Coche - Composition</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPower(10)">Disminuir</button>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const brand = "Audi";
    const model = "A4";
    // const power = 40;
    let power = ref(40);

    const upPower = () => {
      console.log("Aumentar potencia...");
      power.value++;
      console.log(power.value);
    };

    const downPower = (newPower) => {
      console.log("Bajar potencia..." + newPower);
      power.value = power.value - newPower;
      console.log(power.value);
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
