<template>
  <div class="navigation">
    <div class="navs">
      <div
        v-for="(nav, key) in navs"
        :key="key"
        class="item"
        @click="chageTab(nav.key)"
      >
        {{ nav.title }}
      </div>
    </div>

    <div class="tabs">
      <template v-if="currentTab === 'top'">
        <Top />
      </template>
      <template v-if="currentTab === 'about'">
        <About />
      </template>
      <template v-if="currentTab === 'works'">
        <Works />
      </template>
      <template v-if="currentTab === 'skils'">
        <Skils />
      </template>
      <template v-if="currentTab === 'outputs'">
        <Outputs />
      </template>
      <template v-if="currentTab === 'contacts'">
        <Contacts />
      </template>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Top from '~/components/Top.vue'
import About from '~/components/About.vue'
import Works from '~/components/Works.vue'
import Skils from '~/components/Skils.vue'
import Outputs from '~/components/Outputs.vue'
import Contacts from '~/components/Contacts.vue'

export default Vue.extend({
  components: {
    Top,
    About,
    Works,
    Skils,
    Outputs,
    Contacts
  },
  data() {
    return {
      currentTab: 'top',
      navs: [
        { title: 'Top', key: 'top' },
        { title: 'About', key: 'about' },
        { title: 'Works', key: 'works' },
        { title: 'Skils', key: 'skils' },
        { title: 'Outputs', key: 'outputs' },
        { title: 'Contacts', key: 'contacts' }
      ]
    }
  },
  methods: {
    chageTab(key) {
      this.currentTab = key
    }
  }
})
</script>

<style lang="scss" scoped>
.navigation {
  position: relative;
}

.navs {
  text-align: center;
  margin: 10px 10px 10px 10px;
}

.nav {
  position: fixed;
  width: 100%;
  text-align: center;
}
.item {
  display: inline-block;
  margin: 0px 9px;
}
// .tabs {
//   margin-top: 10px;
// }
</style>
