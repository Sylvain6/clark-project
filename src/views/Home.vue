<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import axios from 'axios';

axios.get('https://api.ozae.com/gnw/articles?date=20190317__20190317&edition=fr-fr&key=11116dbf000000000000960d2228e999&hard_limit=50&topic=s')
  .then(response => console.log(response));

export default {
  name: 'home',
  components: {
    HelloWorld,
  },
};
</script>
