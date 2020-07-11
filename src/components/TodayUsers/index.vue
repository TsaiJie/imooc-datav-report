<template>
  <common-card
    title="今日交易用户数"
    value=" 39,165">
    <template v-slot:footer>
      <div>
        <span>退货率 </span>
        <span class="emphasis">5.14%</span>
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

<style scoped>

</style>
