<template>
  <common-card title="今日交易用户数"
               value=" 39,165">
    <template v-slot:footer>
      <div class="compare-wrapper">
        <div class="compare">
          <span>日同比</span>
          <span class="emphasis">7.33%</span>
          <div class="increase"></div>
        </div>
        <div class="compare">
          <span>月同比</span>
          <span class="emphasis">17.33%</span>
          <div class="decrease"></div>
        </div>
      </div>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from '../../mixins/commonCardMixin'

export default {
  mixins: [commonCardMixin]
}
</script>

<style lang="scss" scoped>

  .compare-wrapper {
    display: flex;
  }
</style>
