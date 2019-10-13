<template>
  <div id="app">
    <header>
      <div class="navbar tabs is-toggle is-fullwidth">
        <ul>
          <li v-for="(tab, key) in tabs" :key="key" @click="chageTab(tab.key)">
            {{ tab.title }}
          </li>
        </ul>
      </div>
    </header>
    <template v-if="currentTab === 'top'">
      <Top>Top</Top>
    </template>
    <template v-if="currentTab === 'about'">
      <About>About</About>
    </template>
    <template v-if="currentTab === 'works'">
      <Works>Works</Works>
    </template>
    <template v-if="currentTab === 'skils'">
      <Skils>Skils</Skils>
    </template>
    <template v-if="currentTab === 'outputs'">
      <Outputs>Outputs</Outputs>
    </template>
    <template v-if="currentTab === 'contacts'">
      <Contacts>Contact</Contacts>
    </template>
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
      tabs: [
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

<style>
.header {
  position: fixed;
  z-index: 10;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
