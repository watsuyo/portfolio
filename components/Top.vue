<template>
  <div class="group">
    <Content
      content-text-name
      :img="
        'https://1.bp.blogspot.com/-Iv3bczeEefY/WxvJvlRTqEI/AAAAAAABMjc/9Rw8cVYk4B8P8_bcvXoA6gpLuByjtsPdQCLcBGAs/s800/computer_school_boy.png'
      "
      :my-name="'Tsuyoshi Hirosawa'"
      :content-text="['Web Developer']"
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
