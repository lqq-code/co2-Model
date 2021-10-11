<template>
  <div class="site1_contanier">
    <div id="myChart"></div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      drawer: false
    }
  },
  computed: {},
  methods: {
    echartsInit() {
      // 找到容器
      let myChart = this.$echarts.init(document.getElementById('myChart'))
      // 开始渲染
      myChart.setOption({
        title: { text: '我就试试' },
        tooltip: {},
        xAxis: {
          data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子']
        },
        yAxis: {},
        series: [
          {
            name: '销量',
            type: 'bar',
            data: [5, 20, 36, 10, 10, 20]
          }
        ]
      })
    }
  },
  mounted() {
    this.echartsInit()
  }
}
</script>
<style scope>
#myChart {
  width: 600px;
  height: 300px;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
</style>
