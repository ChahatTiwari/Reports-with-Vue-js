<template>
  <div class="my-card2">
    <b class="bartext">Total Active Users</b>
    <apexchart
      type="bar"
      height="270"
      width="700"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </div>
 
</template> 
<script>
import VueApexCharts from "vue3-apexcharts";
import { getCssVar } from "quasar";

export default {
  name: "barGraph",

  components: {
    apexchart: VueApexCharts,
  },
  data: function () {
    return {
      chartOptions: {
        chart: {
          type: "bar",
          height: 350,
          toolbar: { show: false },
        },
        plotOptions: {
          bar: {
            horizontal: false,
            columnWidth: "40%",
            endingShape: "rounded",
          },
        },
        dataLabels: {
          enabled: false,
        },

        stroke: {
          show: true,
          width: 0,
          colors: ["transparent"],
        },
        xaxis: {
          categories: ["Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep"],
        },
        yaxis: { opposite: true, min: 0, max: 40, tickAmount: 8 },
        fill: {
          opacity: 1,
        },

        colors: ["#006400", "#FF0000", getCssVar("primary")],
        grid: {
          borderColor: "#000000",
        },
      },

      series: [
        {
          name: "Elite",
          data: [8, 5, 7, 6, 21, 8, 6, 6],
        },
        {
          name: "Pro",
          data: [17, 23, 10, 23, 15, 11, 21, 12],
        },
        {
          name: "Comunity",
          data: [10, 11, 6, 35, 18, 22, 23, 11],
        },
      ],
    };
  },
  
};
</script>
<style scoped>
.bartext {
  font-size: 1.4em;
  padding-left: 30px; 
}
</style>