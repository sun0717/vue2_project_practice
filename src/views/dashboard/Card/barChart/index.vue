<template>
    <!-- 容器 -->
    <div class="charts" ref="charts"></div>
  </template>
  
  <script>
  // 引入echarts
  import echarts from "echarts";
  export default {
    name: "barChart",
    mounted() {
      // 初始化echarts实例
      let lineCharts = echarts.init(this.$refs.charts);
      // 配置数据
      lineCharts.setOption({
        xAxis: {
          show: false,
          // 均分
          type: 'category'
        },
        yAxis: {
          // 隐藏y轴
          show: false,
        },
        // 系列
        series: [
          {
            // 图表形式-柱状图
            type: "bar",
            data: [10, 7, 3, 12, 21, 9, 16, 10, 4, 8, 17, 8],
            color: 'purple'
          },
        ],
        // 布局调试
        grid: {
          left: 0,
          top: 0,
          right: 0,
          bottom: 0,
        },
        tooltip: {

        }
      });
    },
  };
  </script>
  
  <style scoped>
  .charts {
    width: 100%;
    height: 100%;
  }
  </style>