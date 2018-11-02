<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import $HTTP from '../api/index.js'
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  mounted() {
    console.log(123123);
    $HTTP.GET('/head').then(res => {
      console.log(res, 11111);
    })
    $HTTP.GET('/health').then(res => {
      console.log(res, 222222);
    })
    $HTTP.GET('/test').then(res => {
      console.log(res, 33333);
    })
    $HTTP.GET('/hello/黑皮').then(res => {
      console.log(res, 44444);
    })
  }
}
</script>
