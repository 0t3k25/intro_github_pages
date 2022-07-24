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
        labels: ['初音ミク', 'MMD', 'MME', 'SWITCH(GAME)', '読書'],
        datasets: [
          {
            label: 'HOBBY',
            backgroundColor: '#FFE4B5',
            borderColor: '#FFE4B5',
            pointBackgroundColor: '#FFE4B5',
            pointBorderColor: '#fff',
            pointHoverBackgroundColor: '#fff',
            pointHoverBorderColor: '#FFE4B5',
            data: [5, 2, 1, 2, 3],
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
