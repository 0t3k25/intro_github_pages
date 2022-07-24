<template>
  <Radar
    :chart-options="chartOptions"
    :chart-data="chartData"
    :chart-id="chartId"
    :dataset-id-key="datasetIdKey"
    :plugins="plugins"
    :css-classes="cssClasses"
    :styles="styles"
    :width="width"
    :height="height"
  />
</template>

<script lang="ts">
import { Radar } from 'vue-chartjs/legacy'

import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  PointElement,
  LineElement,
  RadialLinearScale,
} from 'chart.js'

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  PointElement,
  RadialLinearScale,
  LineElement
)

export default {
  name: 'RadarChart',
  components: {
    Radar,
  },
  props: {
    chartId: {
      type: String,
      default: 'radar-chart',
    },
    datasetIdKey: {
      type: String,
      default: 'label',
    },
    width: {
      type: Number,
      default: 250,
    },
    height: {
      type: Number,
      default: 250,
    },
    cssClasses: {
      default: '',
      type: String,
    },
    styles: {
      type: Object,
      default: () => {},
    },
    plugins: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      chartData: {
        labels: ['HTML/CSS', 'javascript', 'php', 'python', 'flask'],
        datasets: [
          {
            label: 'JOB',
            backgroundColor: '#ffc0cb',
            borderColor: '#ffc0cb',
            pointBackgroundColor: '#ffc0cb',
            pointBorderColor: '#fff',
            pointHoverBackgroundColor: '#fff',
            pointHoverBorderColor: '#ffc0cb',
            data: [3, 2, 2, 2, 1],
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scale: {
          r: {
            suggestedMin: 0,
            suggestedMax: 5,
          },
          ticks: {
            stepSize: 1,
          },
        },
      },
    }
  },
}
</script>
