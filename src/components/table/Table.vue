<template>
  <table>
    <thead>
      <tr>
        <th></th>
        <th>First name</th>
        <th>Last name</th>
        <th>Participation</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(firstName, index) in firstName" :key="index">
        <td class="indice">{{ index + 1 }}</td>
        <td class="label">{{ firstName }}</td>
        <td class="label">{{ lastName[index] }}</td>
        <td class="label">{{ values[index] }}%</td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  name: "Table",
  props: {
    firstName: Array,
    lastName: Array,
    values: Array,
  },
  mounted() {
    console.log(this.firstName);
  },
};
</script>

<style>
th {
  border: 1px solid #cdcdcd;
  padding: 10px;
}
table {
  border-collapse: collapse;
}

.label {
  border: 1px solid #cdcdcd;
  padding: 10px;
  width: 100px;
  text-align: justify;
}
.indice {
  border: 1px solid #cdcdcd;
  padding: 10px;
  width: 50px;
  text-align: center;
}
</style>