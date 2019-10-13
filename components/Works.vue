<template>
  <div>
    <div>
      2019.01~
    </div>
    <div>
      Omnis, inc. Fashion Tech Venture Nuxt.js Vue.js TypeScript
    </div>
    <div>
      OriginalServise
    </div>
    <div>
      Yotei-kun
    </div>
    <div>
      Yotei-kun can authenticate with GitHub, make a schedule and take
      attendance Node.js
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      items: [
        {
          title: 'Yotei-kun',
          description: 'GitHubで認証でき、予定を作って出欠が取れるサービス',
          link: 'https://mr-schedule-arranger.herokuapp.com/'
        },
        {
          title: 'niiyama-project',
          description:
            'アーティストの活動休止を受け、ファンが想いを発信できるサイト',
          link: 'https://niiyama-project-0210.firebaseapp.com/'
        }
      ]
    }
  }
})
</script>

<style>
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
.serviceTop {
  padding: 5%;
}
</style>
