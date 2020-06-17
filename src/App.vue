<template>
  <div id="app">
    <login></login>
  </div>
</template>

<script>
import login from './login'
import './assets/style/style.css';

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    login
  }

}
</script>

<style>

</style>
