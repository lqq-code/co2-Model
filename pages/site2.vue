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
      $.get('https://test-eagle.oss-cn-shenzhen.aliyuncs.com/notarization/all_json.json', function(_rawData) {
        console.log('_rawData', _rawData)
        let timeKey = Object.keys(_rawData.Max)
        let timeValue = Object.values(_rawData.Max)
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
          yAxis: { name: 'co2' },
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
              name: 'co2',
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
                    yAxis: 600
                  },
                  {
                    yAxis: 800
                  },
                  {
                    yAxis: 1000
                  },
                  {
                    yAxis: 1200
                  },
                  {
                    yAxis: 1400
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
.site1_contanier {
  padding-top: 50px;
}
#myChart {
  width: 100%;
  height: 300px;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
</style>
