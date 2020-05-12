<template>
  <div id="g2" class="g2"></div>
</template>

<script>
  import { Chart } from '@antv/g2';

  export default {
    name: "G2",
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

        const chart = new Chart({
          container: 'g2',
          width: 600,
          height: 300
        })

        chart.data(data)

        chart
          .interval()
          .position('genre*sold')

        chart.render()
      }
    }
  }
</script>

<style scoped>

</style>
