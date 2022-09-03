<template>
  <div id="chart">
      <q-card class="my-card">
      <label>User Reports</label>
      <q-card-section class="bar">
        <apexcharts
          type="donut"
          width="235"
          :options="optionsDonut1"
          :series="seriesDonut1"
        ></apexcharts>
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <label>Registration Reports</label
      ><q-card-section class="bar">
        <apexcharts
          type="donut"
          width="235"
          :options="optionsDonut2"
          :series="seriesDonut2"
        ></apexcharts>
      </q-card-section>
    </q-card>
    <q-card class="my-card">
      <label>Earning Reports</label
      ><q-card-section class="bar">
        <apexcharts
          type="donut"
          width="235"
          :options="optionsDonut3"
          :series="seriesDonut3"
        ></apexcharts>
      </q-card-section>
    </q-card>
    <q-card class="my-card">
      <label>Mobile Reports</label
      ><q-card-section class="bar">
        <apexcharts
          type="donut"
          width="235"
          :options="optionsDonut4"
          :series="seriesDonut4"
        ></apexcharts>
      </q-card-section>
    </q-card>
    <q-card class="my-card">
      <label>Coupon Codes History</label
      ><q-card-section class="bar">
        <apexcharts
          type="donut"
          width="235"
          :options="optionsDonut5"
          :series="seriesDonut5"
        ></apexcharts>
      </q-card-section>
    </q-card>
  </div>
  <div class="chart2">
    <barGraph />
    <q-card class="my-card3">
      <q-card-section class="pie">
        <label class="pieText">Servive Accessibility</label>
        <apexcharts
          type="pie"
          width="360"
          :options="optionsPie"
          :series="seriesPie"
        ></apexcharts>
      </q-card-section>
    </q-card>
  </div>
  <div id="lineGraph">
    <LineGraph></LineGraph>
    <LineGraph2></LineGraph2>
  </div>

  <div class="lastG">
    <LastGraphs></LastGraphs>
  </div>
</template>

<script>
import barGraph from "src/pages/barGraph.vue";
import VueApexCharts from "vue3-apexcharts";
import LineGraph from "src/pages/lineGraph.vue";
import LastGraphs from "../pages/lastGraphs.vue";
import LineGraph2 from "src/pages/lineGraph2.vue";
import { getCssVar } from "quasar";

export default {
  name: "MainLayout",

  components: {
    apexcharts: VueApexCharts,
    barGraph,
    LineGraph,
    LastGraphs,
    LineGraph2,
  },

  data: function () {
    return {
      optionsDonut1: {
        dataLabels: {
          enabled: false,
        },
        labels: ["Active Users", "in Active users", "Pending Users"],
        plotOptions: {
          pie: {
            donut: {
              size: "80%",

              labels: {
                show: true,

                total: {
                  show: true,
                  showAlways: true,

                  fontSize: "10px",

                  // color: "#03fc14",
                },
              },
            },
          },
        },
        legend: { position: "bottom" },
        colors: [getCssVar("positive"), "#FF0000", getCssVar("primary")],
      },
      seriesDonut1: [44, 55, 41],

      optionsDonut2: {
        dataLabels: {
          enabled: false,
        },
        labels: ["Comunity", "Elite", "Pro"],
        plotOptions: {
          pie: {
            donut: {
              size: "80%",

              labels: {
                show: true,

                total: {
                  show: true,
                  showAlways: true,

                  fontSize: "10px",

                  // color: "#03fc14",
                },
              },
            },
          },
        },
        legend: { position: "bottom" },
        colors: [getCssVar("positive"), "#FF0000", getCssVar("primary")],
      },
      seriesDonut2: [44, 55, 41],

      optionsDonut3: {
        dataLabels: {
          enabled: false,
        },
        labels: ["Elite", "Skill Pack", "Pro"],
        plotOptions: {
          pie: {
            donut: {
              size: "80%",

              labels: {
                show: true,

                total: {
                  show: true,
                  showAlways: true,

                  fontSize: "10px",

                  // color: "#03fc14",
                },
              },
            },
          },
        },
        legend: { position: "bottom" },
        colors: [getCssVar("positive"), "#FF0000", getCssVar("primary")],
      },
      seriesDonut3: [44, 55, 41],

      optionsDonut4: {
        dataLabels: {
          enabled: false,
        },
        labels: ["Elite", "Pro", "Community"],
        plotOptions: {
          pie: {
            donut: {
              size: "80%",

              labels: {
                show: true,

                total: {
                  show: true,
                  showAlways: true,

                  fontSize: "10px",

                  // color: "#03fc14",
                },
              },
            },
          },
        },
        legend: { position: "bottom" },
        colors: [getCssVar("positive"), "#FF0000", getCssVar("primary")],
      },
      seriesDonut4: [44, 55, 41],

      optionsDonut5: {
        dataLabels: {
          enabled: false,
        },
        labels: ["Elite", "Pro", "Community"],
        plotOptions: {
          pie: {
            donut: {
              size: "80%",

              labels: {
                show: true,

                total: {
                  show: true,
                  showAlways: true,

                  fontSize: "10px",

                  // color: "#03fc14",
                },
              },
            },
          },
        },
        legend: { position: "bottom" },
        colors: [getCssVar("positive"), "#FF0000", getCssVar("primary")],
      },
      seriesDonut5: [44, 55, 41],
      optionsPie: {
        dataLabels: {
          enabled: false,
        },
        labels: ["Aspen", "Cyber Q", "Code Red", "First Look", "Cyber Talks"],
        colors: [
          getCssVar("positive"),
          "#FF0000",
          getCssVar("primary"),
          "#f2f2f2",
          "#FFA500",
        ],
      },
      seriesPie: [65, 40, 41, 33, 12],
    };
  },
};
</script>
<style scoped>
#chart {
  margin-top: 4px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  height: 300px;
  gap: 1.5em;

  text-align: center;
  background-color: #f2f2f2;
}

#chart:hover {
  visibility: black;
}
.my-card {
  width: 18%;
  height: 230px;
  border-radius: 7%;
  margin-top: 24px;
  /* margin-left: 14px; */
}
.my-card:hover {
  background-color: black;
}
.bar {
  margin-left: -28px;
}
.chart2 {
  margin-top: 50px;
  margin-left: 12px;
  display: flex;
  flex-direction: row;
  gap: 09.5em;
}

.my-card3 {
  height: 260px;
  width: 30%;
  /* text-align: center; */
}
#Graph11 {
  width: 500px;
}
.pieText {
  padding-left: 88px;
  font-size: 1.3em;
}
#lineGraph {
  display: flex;
  flex-direction: row;

  margin-top: 50px;
}
</style>
 