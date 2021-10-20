<template>
  <div class="site1_contanier">
    <div id="myChart"></div>
  </div>
</template>

<script>
import moment from 'moment'
export default {
  components: {},
  data() {
    return {}
  },
  computed: {},
  methods: {
    echartsInit() {
      // 找到容器
      let myChart = this.$echarts.init(document.getElementById('myChart'))
      $.get('https://test-eagle.oss-cn-shenzhen.aliyuncs.com/notarization/sep1.json', function(_rawData) {
        let timeKey = Object.keys(_rawData.value)
        let timeValue = Object.values(_rawData.value)
        let timeTemp = []
        for (let i = 0; i < timeKey.length; i++) {
          timeTemp.push(moment(parseInt(timeKey[i])).format('YYYY-MM-DD HH:mm:ss'))
        }
        // 开始渲染

        myChart.setOption({
          animationDuration: 10000,
          title: { text: 'David Derham Lecture Theatre' },
          tooltip: {
            trigger: 'axis',
            axisPointer: {
              type: 'cross',
              label: {
                backgroundColor: '#6a7985'
              }
            }
          },
          xAxis: {
            data: timeTemp,
            boundaryGap: [0, '100%']
          },
          yAxis: { boundaryGap: [0, '100%'], name: 'CO2' },
          toolbox: {
            right: 10,
            feature: {
              dataZoom: {
                yAxisIndex: 'none'
              },
              restore: {},
              saveAsImage: {}
            }
          },
          dataZoom: [
            {
              startValue: '2014-06-01'
            },
            {
              type: 'inside'
            }
          ],
          series: [
            {
              name: 'CO2',
              type: 'line',
              data: timeValue,
              markLine: {
                silent: true,
                lineStyle: {
                  color: '#333'
                },
                data: [
                  {
                    yAxis: 400
                  },
                  {
                    yAxis: 500
                  },
                  {
                    yAxis: 300
                  }
                ]
              }
            }
          ]
        })
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
  width: 100%;
  height: 300px;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
</style>
