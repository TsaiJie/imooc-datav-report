<template>
  <common-card title="累计用户数"
               value=" 39,165">
    <template>
      <div id="total-users-chart" :style="{width: '100%', height: '100%'}"></div>
    </template>
    <template v-slot:footer>
      <div class="total-users-footer">
        <span>日同比</span>
        <span class="emphasis">7.33%</span>
        <div class="increase"></div>
        <span class="month">月同比</span>
        <span class="emphasis">7.33%</span>
        <div class="decrease"></div>
      </div>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from '../../mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin],
  mounted () {
    const chartDom = document.getElementById('total-users-chart')
    const chart = this.$echarts.init(chartDom)
    chart.setOption({
      grid: {
        left: 0,
        right: 0,
        bottom: 0,
        top: 0
      },
      xAxis: {
        type: 'value',
        show: false
      },
      yAxis: {
        type: 'category',
        show: false
      },
      series: [{
        stack: '总量',
        type: 'bar',
        barWidth: 10,
        data: [200],
        itemStyle: {
          color: '#45c946'
        }
      }, {
        stack: '总量',
        type: 'bar',
        data: [300],
        itemStyle: {
          color: '#eee'
        }
      }]
    })
  }
}
</script>

<style lang="scss" scoped>
  .total-users-footer {
    display: flex;
    align-items: center;
    .month {
      margin-left: 10px;
    }
  }

</style>
