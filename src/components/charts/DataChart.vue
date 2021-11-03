<template>
  <div>
    <div style="max-width: 600px; widht:500px">
      <vue3-chart-js style="width:400px" v-bind="{ ...doughnutChart }" />
    </div>
  </div>
</template>

<script>
import Vue3ChartJs from "@j-t-mcc/vue3-chartjs";

export default {
  name: "App",
  props:{
    firstName: Array,
    values: Array,
    lastName: Array,
  },
  components: {
    Vue3ChartJs,
  },
  setup(props) {
    let label = [];
    props.lastName.map((item, index)=>{
      label.push(`${props.firstName[index]} ${item}`)
    })
    const doughnutChart = {
      type: "doughnut",
      data: {
        labels: label,
        datasets: [
          {
            backgroundColor: ["#2c96dd", "#bcc3c7", "#9c55b8", "#e94a35", "#15ba9a"],
            data: props.values,
          },
        ],
      },
      options: {
        plugins: {
            legend: {
                position:'right',
                display: true,
                borderRadius:2,
                labels: {
                    boxWidth: 30,
                    boxHeight: 25,
                    font: {
                        size: 14,
                        weight: 'bold'
                    }
                }
            }
        }
    }
    };

    return {
      doughnutChart,
    };
  },
};
</script>
