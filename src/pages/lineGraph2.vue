<template>
  <div id="Linechart">
    <b class="line2text">Awaiting Payment Report</b
    ><apexchart
      type="line"
      width="300"
      height="220"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </div>
</template>
<script>
import VueApexCharts from "vue3-apexcharts";

export default {
  name: "lineGraph2",

  components: {
    apexchart: VueApexCharts,
  },

  data: function () {
    return {
      series: [
        {
          name: "Community",
          data: [1, 15, 25, 30, 50, 80],
        },
        {
          name: "Pro",
          data: [4, 18, 27, 24, 42, 60],
        },
        {
          name: "Elite",
          data: [3, 12, 28, 39, 47, 57],
        },
      ],
      chartOptions: {
        chart: {
          height: 350,
          type: "line",
          dropShadow: {
            enabled: true,
            color: "#000",
            top: 18,
            left: 7,
            blur: 10,
            opacity: 0.2,
          },
          toolbar: {
            show: false,
          },
        },
        colors: ["#006400", "#FF0000", "#0000FF"],
        // dataLabels: {
        //   enabled: true,
        // },
        stroke: { width: 1 },
        markers: { size: [4, 4, 4] },

        grid: {
          borderColor: "#000000",
        },

        xaxis: {
          categories: [
            "15 Jan",

            "15 Feb",
            "15 Mar",
            "15 Apr",
            "15 May",
            "15 Jun",
          ],
        },
        yaxis: {
          min: 0,
          max: 100,
          tickAmount: 5,
          opposite: "true",
        },
        legend: {
          position: "bottom",
          horizontalAlign: "left",
          floating: true,
          offsetY: 127,
          offsetX: 15,
        },
      },
    };
  },
};
</script>
<style scoped>
#Linechart {
  margin-left: 23px;
}
.line2text {
  font-size: 1.3em;
}
</style>
