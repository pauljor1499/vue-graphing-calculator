<template></template>

<script>
import Desmos from "desmos";

export default {
  name: "Calculator",

  setup() {
    const elt = document.createElement("div");
    elt.style.width = "600px";
    elt.style.height = "400px";

    const calculator = Desmos.GraphingCalculator(elt);
    calculator.setExpression({ id: "graph1", latex: "y=x^2" });

    document.body.prepend(elt);

    return {};
  },
};
</script>

<style scoped>
#calculator {
  margin: auto;
  border: 1px solid black;
}
</style>
