<template>
  <div class="group">
    <Content
      :content-text="[
        `2019.01~`,
        'Omnis, inc.',
        'Fashion Tech Venture',
        'Nuxt.js Vue.js TypeScript',
        'OriginalServises',
        'Yotei-kun',
        'make a schedule and take attendance',
        'Node.js'
      ]"
      :title="'Works'"
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
  margin-top: 15%;
}
</style>
