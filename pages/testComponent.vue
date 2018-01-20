<template>
  <div class="test-component">
    <h1>this is the component</h1>
    <div v-for="(item, index) in information" :key="index">
     {{index}} {{item.id}} {{item.name}}</div>
    <a href="https://github.com/nuxt/nuxt.js"
      target="_blank"
      class="button--grey">GitHub</a>
  </div>
</template>
<script>
  import info from "../Mocks/mockTest"
  export default {
    layout: 'testNuxt',
    data () {
      return {
        info,
        item: false,
        information: [
          {
            id: 1,
            name: 'kris'
          },
          {
            id: 2,
            name: 'andi'
          }
        ]
      }
    },
    created () {
      console.log(this.information)
    }
  }
</script>
