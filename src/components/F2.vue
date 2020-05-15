<template>
  <div>
     <canvas id="myChart" width="400" height="260"></canvas>
  </div>
</template>

<script>
  import F2 from '@antv/f2'

  export default {
    name: "F2",
    mounted() {
      this.initChart()
    },
    methods: {
      initChart () {
        const data = [
          { genre: 'Sports', sold: 275 },
          { genre: 'Strategy', sold: 115 },
          { genre: 'Action', sold: 120 },
          { genre: 'Shooter', sold: 350 },
          { genre: 'Other', sold: 150 },
        ]

        const chart = new F2.Chart({
          id: 'myChart',
          pixelRatio: window.devicePixelRatio // 指定分辨率
        })

        chart.source(data)

        chart
          .interval()
          .position('genre*sold')
          .color('genre')

        chart.render()
      }
    }
  }
</script>

<style scoped>

</style>
