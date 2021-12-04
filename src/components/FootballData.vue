<template>
  <div>
    {{ info }}
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Football Data',
  data() {
    return {
      info: null,
    }
  },
  mounted() {
    // axios
    //   .get('https://api.coindesk.com/v1/bpi/currentprice.json')
    //   .then((response) => (this.info = response))

    const config = {
      headers: {
        Authorization: `Bearer ${process.env.VUE_APP_FOOTBALL_API_KEY}`,
      },
    }

    axios
      .get('http:localhost:8080/conferences', config)
      .then((response) => console.log(response))
      .catch((error) => console.log(error))
  },
}
</script>
  
<style lang="scss">
</style>