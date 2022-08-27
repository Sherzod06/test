<template>
  <div class="bg-slate-200 px-24 py-10">
    <div class="grid grid-cols-3 gap-6">
      <div class="bg-white flex items-center p-4 rounded-md">
        <div class="p-1 mr-2 w-16 bg-amber-200 rounded-md">
          <PaperClipIcon class="text-amber-500" />
        </div>
        <div>
          <div class="text-xs">Jami to'langan summa</div>
          <div>
            1 684 000 000 sum
          </div>
        </div>
      </div>
      <div class="bg-white flex items-center p-4 rounded-md">
        <div class="p-1 mr-2 w-16 bg-amber-200 rounded-md">
          <PaperClipIcon class="text-amber-500" />
        </div>
        <div>
          <div class="text-xs">Jami so'ralgan summa</div>
          <div>
            1 684 000 000 sum
          </div>
        </div>
      </div>
      <div class="bg-white flex items-center p-4 rounded-md">
        <div class="p-1 mr-2 w-16 bg-amber-200 rounded-md">
          <PaperClipIcon class="text-amber-500" />
        </div>
        <div>
          <div class="text-xs">To'lanishi kerak summa</div>
          <div>
            1 684 000 000 sum
          </div>
        </div>
      </div>
    </div>
    <div class="rounded-md bg-white mt-8 p-5">
      <h1 class="text-2xl font-bold">Homiylar va talabalar soni</h1>
      <div>
        <LineChart :chart-data="testData" :options="options" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { PaperClipIcon } from '@heroicons/vue/solid'
import { LineChart } from 'vue-chart-3'
import { Chart, registerables } from 'chart.js'

Chart.register(...registerables)
const options = {
  elements: {
    line: {
      tension: 0.4
    }
  }
}

const testData = {
  labels: [],
  datasets: [
    {
      label: 'Homiylar',
      data: [],
      borderColor: '#FF6384',
      backgroundColor: '#FFB1C1',
      fill: 'start'
    },
    {
      label: 'Talabalar',
      data: [],
      borderColor: '#DD8F51',
      backgroundColor: '#DD8F51',
      fill: 'start'
    }
  ]
}


</script>

<style scoped>
</style>