<template>
  <div id="app">
    <input
      v-model="tituloetuiqueta"
      placeholder="escribe un nombre"
      type="text"
    />
    <div class="clase">
      <div class="conteiner">
        <row>
          <col-12>
            <TableDat :superdata="trabajadores" />
          </col-12>
        </row>
      </div>
    </div>
    <CardsPrueba :infod="tituloetuiqueta" />
  </div>
</template>

<script>
import TableDat from "@/components/TableDat.vue";
import CardsPrueba from "@/components/CardsPrueba.vue";
export default {
  name: "App",
  data() {
    return {
      tituloetuiqueta: "QQQQQQQQQQQQQ",
      ndata: "",
      trabajadores: [
        {
          nombre: "Franco Urra",
          edad: 47,
          rut: "12345678-9",
          diagnostico: "Hipertensión Arterial",
        },
        {
          nombre: "Matías Mesa",
          edad: 27,
          rut: "12345678-9",
          diagnostico: "Diabetes Mellitus 1",
        },
        {
          nombre: "Enrique Flores",
          edad: 37,
          rut: "12345678-9",
          diagnostico: "Disfunción de la vista",
        },
        {
          nombre: "Milagros Acosta",
          edad: 17,
          rut: "12345678-9",
          diagnostico: "Hipertensión Pulmonar",
        },
        {
          nombre: "Victor Fernandez",
          edad: 47,
          rut: "12345678-9",
          diagnostico: "Diabetes Mellitus 2",
        },
        {
          nombre: "Is Pinto",
          edad: 15,
          rut: "12345678-9",
          diagnostico: "Pancreatitis Aguda",
        },
        {
          nombre: "Francisco Lobos",
          edad: 2,
          rut: "12345678-9",
          diagnostico: "Neuroblastoma",
        },
        {
          nombre: "Jean Jaque",
          edad: 67,
          rut: "12345678-9",
          diagnostico: "Enfermedad de Parkinson",
        },
        {
          nombre: "Cesar Riveros",
          edad: 87,
          rut: "12345678-9",
          diagnostico: "Alopecia por Radiación",
        },
        {
          nombre: "Joshua Espinoza",
          edad: 77,
          rut: "12345678-9",
          diagnostico: "Enfermedad de Creutzfeldt-Jakob",
        },
      ],
    };
  },
  components: {
    TableDat,
    CardsPrueba,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
