<template>
  <div class="group">
    <Content :content-text="['connpass', 'Qiita', 'note']" :title="'Outputs'" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Content from '~/components/Content.vue'

export default Vue.extend({
  components: {
    Content
  }
})
</script>

<style lang="scss" scoped>
.group {
  text-align: center;
  margin-top: 15%;
}
</style>
