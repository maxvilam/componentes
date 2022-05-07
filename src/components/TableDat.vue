<template>
  <table class="table">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">nombre</th>
        <th scope="col">rut</th>
        <th scope="col">diagnostico</th>
      </tr>
    </thead>
    <tbody v-if="superdata.length > 0">
      <tr v-for="(trabajador, i) in superdata" :key="i">
        <th>{{ i + 1 }}</th>
        <td>{{ trabajador.nombre }}</td>
        <td>{{ trabajador.rut }}</td>
        <td>@{{ trabajador.diagnostico }}</td>
      </tr>
    </tbody>
    <tbody v-else>
      <tr>
        <td colspan="4">sin data</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: "TableDat",
  props: {
    superdata: {
      type: Array,
      default: () => [] /* el valor por defecto */,
    },
  },
};
</script>

<style></style>
