<template>
  <div id="componente">
    <h1>Notas</h1>
    <h1>Resultado académico</h1>
    <label for="nota"></label>Introduzca su nota
    <input
      type="number"
      v-model="nota"
      name="nota"
      id="nota"
      placeholder="Indique su nota"
    />
    <button @click="calificacion">Enviar</button>
    <div id="res">
      <p>{{ message }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Notas",
  data: () => ({
    nota: "",
    message: "",
  }),
  methods: {
    calificacion() {
      console.log("hola");
      let nota = this.nota;

      if (nota < 3 && nota >= 0) {
        this.message = "Muy deficiente";
      }
      if (nota >= 3 && nota < 5) {
        this.message = "Inuficiente";
      }
      if (nota < 6 && nota >= 5) {
        this.message = "Suficiente";
      }
      if (nota >= 6 && nota < 7) {
        this.message = "Bien";
      }
      if (nota >= 7 && nota < 9) {
        this.message = "Notable";
      }
      if (nota >= 9) {
        this.message = "Sobresaliente";
      }
    },
  },
};
</script>
