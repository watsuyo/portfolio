<template>
  <div>
    <div>
      25 years old
    </div>
    <div>
      Omnis, inc.
    </div>
    <div>
      Front-End Engineer
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      abouts: [
        {
          title: 'Profile',
          item1: 'Place of birth: 埼玉県',
          item2: 'Sports: 野球(埼玉西武ライオンズ)',
          item3: 'Music: 福山雅治、新山詩織、Awesome City Club'
        },
        {
          title: 'Career',
          item1: 'Job: 2019年1月からWebエンジニア',
          item2: 'Languages: Vue.js,Node.js,Golang',
          item3: 'Details... ',
          url:
            'https://www.wantedly.com/secret_profiles/Sv39_lCK1jbuki5TNuJScbujIjBvqQpU',
          wantedly: 'Wantedlyに詳しい情報があります'
        }
      ]
    }
  }
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.aboutTop {
  padding: 5%;
}
</style>
