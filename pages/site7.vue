<template>
  <div class="site2_contanier">
    <el-page-header @back="goBack" content="Chemistry teaching room"> </el-page-header>
    <div id="myChart"></div>
    <div id="myChartP"></div>
    <div id="myChart2"></div>
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
    goBack() {
      window.history.go(-1)
    },
    echartsInit() {
      // 找到容器
      let myChart = this.$echarts.init(document.getElementById('myChart'))
      $.get('https://test-eagle.oss-cn-shenzhen.aliyuncs.com/zdG0Ga/chemistry_teachinng_room.json', function(_rawData) {
        let timeKey = Object.keys(_rawData.Max)
        let timeValue = Object.values(_rawData.Max)
        let timeTemp = []
        for (let i = 0; i < timeKey.length; i++) {
          timeTemp.push(moment(parseInt(timeKey[i])).format('YYYY-MM-DD HH:mm:ss'))
        }
        // 开始渲染
        myChart.setOption({
          animationDuration: 10000,
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
          yAxis: { name: 'CO2 (in ppm)', scale: true },
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
                    yAxis: 450
                  },
                  {
                    yAxis: 500
                  },
                  {
                    yAxis: 550
                  },
                  {
                    yAxis: 600
                  }
                ]
              }
            }
          ]
        })
      })
      let myChartP = this.$echarts.init(document.getElementById('myChartP'))
      $.get('https://test-eagle.oss-cn-shenzhen.aliyuncs.com/zdG0Ga/chemistry_teachinng_room.json', function(_rawData) {
        const colors = ['#5470C6', '#EE6666']
        let timeKey = Object.keys(_rawData.new_p)
        let timeValue = Object.values(_rawData.new_p)
        let timeTemp = []
        for (let i = 0; i < timeKey.length; i++) {
          timeTemp.push(moment(parseInt(timeKey[i])).format('YYYY-MM-DD HH:mm:ss'))
        }
        // 开始渲染
        myChartP.setOption({
          color: 'green',
          animationDuration: 10000,
          tooltip: {
            trigger: 'axis',
            axisPointer: {
              type: 'cross',
              label: {
                backgroundColor: '#6a7985'
              }
            }
          },
          legend: {},
          xAxis: {
            data: timeTemp,
            boundaryGap: [0, '100%']
          },
          yAxis: { name: 'Probability of infection (%)' },
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
              type: 'line',
              data: timeValue,
              smooth: true,
              emphasis: {
                focus: 'series'
              },
              markLine: {
                silent: true,
                lineStyle: {
                  color: '#333'
                },
                data: [
                  {
                    yAxis: 0
                  },
                  {
                    yAxis: 0.0005
                  },
                  {
                    yAxis: 0.01
                  },
                  {
                    yAxis: 0.015
                  }
                ]
              }
            }
          ]
        })
      })
      let myChart2 = this.$echarts.init(document.getElementById('myChart2'))
      $.get('https://test-eagle.oss-cn-shenzhen.aliyuncs.com/zdG0Ga/chemistry_teachinng_room.json', function(_rawData) {
        const colors = ['#5470C6', '#EE6666']
        let timeKey = Object.keys(_rawData.N)
        let timeValue = Object.values(_rawData.N)
        let timeTemp = []
        let timeValue2
        for (let i = 0; i < timeKey.length; i++) {
          timeTemp.push(moment(parseInt(timeKey[i])).format('YYYY-MM-DD HH:mm:ss'))
        }
        // 开始渲染
        myChart2.setOption({
          color: colors,
          animationDuration: 10000,
          tooltip: {
            trigger: 'axis',
            axisPointer: {
              type: 'cross',
              label: {
                backgroundColor: '#6a7985'
              }
            }
          },
          legend: {},
          xAxis: {
            data: timeTemp,
            boundaryGap: [0, '100%']
          },
          yAxis: { name: 'Occupancy (per person)' },
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
              type: 'line',
              data: timeValue,
              smooth: true,
              emphasis: {
                focus: 'series'
              },
              markLine: {
                silent: true,
                lineStyle: {
                  color: '#333'
                },
                data: [
                  {
                    yAxis: 2
                  },
                  {
                    yAxis: 4
                  },
                  {
                    yAxis: 6
                  },
                  {
                    yAxis: 8
                  },
                  {
                    yAxis: 10
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
.site2_contanier {
  padding-top: 50px;
}
#myChart {
  width: 100%;
  height: 300px;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
#myChartP {
  width: 100%;
  height: 300px;
  margin-top: 50px;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
#myChart2 {
  width: 100%;
  height: 300px;
  margin-top: 50px;
  margin-left: auto;
  margin-right: auto;
  float: left;
}
</style>
