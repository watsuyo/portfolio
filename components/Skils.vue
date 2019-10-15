<template>
  <div class="group">
    <Content
      :content-text="['Nuxt.js', 'Vue.js', 'TypeScript']"
      :title="'Skils'"
    />
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
  margin-top: 10%;
}
</style>
