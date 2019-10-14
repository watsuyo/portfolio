<template>
  <div class="content">
    <img v-if="img" class="content-image" :src="img" />
    <div v-if="title" class="content-title">{{ title }}</div>
    <div class="content-text">
      <div v-if="myName" :class="'content-text-name'">{{ myName }}</div>
      <div class="content-text-right">
        <div v-for="(text, key) in contentText" :key="key">{{ text }}</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    contentTextName: {
      type: Boolean,
      required: false,
      default: false
    },
    img: {
      type: String,
      required: false,
      default: ''
    },
    title: {
      type: Boolean,
      required: false,
      default: false
    },
    myName: {
      type: String,
      required: false,
      default: ''
    },
    contentText: {
      // type: ,
      required: false,
      default: []
    }
  }
})
</script>

<style lang="scss" scoped>
.content {
  display: flex;
  justify-content: center;
  align-items: center;

  &-image {
    text-align: center;
    object-fit: cover;
    height: 15%;
    width: 25%;
    margin: 0 5%;
  }

  &-title {
    text-align: center;
    font-weight: bold;
    font-size: 130%;
    margin: 0 5%;
  }

  &-text {
    display: inline-block;
    line-height: 200%;
    margin: 0 5%;

    &-name {
      font-size: 130%;
      font-weight: bold;
    }

    &-right {
      margin-top: 0%;
    }
  }
}
</style>
