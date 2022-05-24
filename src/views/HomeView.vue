<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" >
    <HelloWorld msg="Is fruit echt gezond?"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
