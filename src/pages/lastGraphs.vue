<template>
  <div class="my-last">
    <div>
      <b class="lasttext1">First Look & Cyber Talks Registration </b>
      <apexchart
        type="bar"
        height="240"
        width="385"
        :options="chartOptions"
        :series="series"
      ></apexchart>
    </div>
    <div>
      <b class="lasttext2">Pro & Elite User Comparision</b
      ><apexchart
        type="bar"
        height="240"
        width="385"
        :options="chartOptions"
        :series="series"
      ></apexchart>
    </div>
    <div>
      <b class="lasttext3">Comunity to Paid Upgrade</b
      ><apexchart
        type="bar"
        height="240"
        width="385"
        :options="chartOptions"
        :series="series"
      ></apexchart>
    </div>
  </div>
</template> 
<script>
import VueApexCharts from "vue3-apexcharts";
export default {
  name: "lastGraph",

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
          categories: [
            "1-7 Days",
            "8-14 Days",
            "15-21 Days",
            "22-30 Days",
            ">30 Days",
          ],
        },
        yaxis: {
          opposite: true,
          min: 0,
          max: 40,
          tickAmount: 8,
        },

        colors: ["#006400", "#FF0000"],
        legend: { position: "bottom" },
        grid: {
          borderColor: "#000000",
        },
      },

      series: [
        {
          name: "Elite",
          data: [4, 5, 7, 6, 7],
        },
        {
          name: "Pro",
          data: [17, 13, 10, 20, 26],
        },
      ],
    };
  },
};
</script>
<style scoped>
.text {
  /* margin-left: 100px; */
}
.my-last {
  display: flex;
  flex-direction: row;
  gap: 1.3em;
  margin-bottom: 130px;
  margin-left: 35px;
  margin-top: 70px;
}
.lasttext1 {
  padding-left: 30px;
  font-size: 01.3em;
}
.lasttext2 {
  padding-left: 30px;
  font-size: 01.3em;
}
.lasttext3 {
  padding-left: 30px;
  font-size: 01.3em;
}
</style> 