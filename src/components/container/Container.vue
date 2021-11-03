<template>
  <div class="main">
    <div class="title">
      <h1>Data</h1>
      <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis</h3>
    </div>
    <div class="contains">
      <div>
        <Table :firstName="firstName" :lastName="lastName" :values="values" />
      </div>
      <div>
        <DataChart :firstName="firstName" :lastName="lastName" :values="values" />
      </div>
    </div>
  </div>
</template>

<script>
import DataChart from "../charts/DataChart.vue";
import Table from "../table/Table.vue";
export default {
  components: {
    DataChart,
    Table,
  },
  data(){
      return{
          firstName: ["Hugo", "Carlos", "Eliza", "Fernanda", "Anderson"],
          lastName: ["Silva", "Moura", "Souza", "Oliveira", "Santos"],
          values: [5, 15, 20, 20, 40],
      }
  }
};
</script>

<style>
.main{
    width: 100%;
}
.contains {
  display: flex;
  justify-content: space-evenly;
    width: 100%;
    align-items: center;

}
</style>