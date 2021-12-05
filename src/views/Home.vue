<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <FootballData />
    <input
      v-model="pincode"
      class="
        shadow
        appearance-none
        border
        rounded
        w-full
        py-2
        px-3
        text-gray-700
        leading-tight
        focus:outline-none focus:shadow-outline
      "
    />
    <p>{{ pincode }}</p>
    <button
      v-on:click="verify"
      class="
        bg-blue-500
        hover:bg-blue-700
        text-white
        font-bold
        py-2
        px-4
        rounded
      "
    >
      Login
    </button>
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
  data() {
    return {
      digit: '',
      //store the pincode
      pincode: '',
    }
  },
  methods: {
    updatePincode() {
      this.pincode = this.digit
    },
    verify() {
      //if the code is correct, push to page with teams etc.
      this.$router.push('/about')
    },
  },
}
</script>
