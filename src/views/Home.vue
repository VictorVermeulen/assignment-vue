<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <FootballData />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import FootballData from '@/components/FootballData.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    FootballData,
  },
}
</script>
