<template>
  <div class="group">
    <Content
      :content-text="[`${myOld} years old`, 'Omnis, inc', 'Front-End Engineer']"
      :title="'About'"
    />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Content from '~/components/Content.vue'

export default Vue.extend({
  components: {
    Content
  },
  data() {
    return {
      myBirthday: {
        year: 1994,
        month: 6,
        day: 2
      }
    }
  },
  computed: {
    myOld() {
      const { year, month, day } = this.myBirthday
      const birthday = new Date(year, month, day)
      const today = new Date()

      const thisYearBirthday = new Date(
        today.getFullYear(),
        birthday.getMonth(),
        birthday.getDate()
      )

      const age = today.getFullYear() - birthday.getFullYear()

      return today < thisYearBirthday ? age - 1 : age
    }
  }
})
</script>

<style lang="scss" scoped>
.group {
  text-align: center;
  margin-top: 10%;
}
</style>
