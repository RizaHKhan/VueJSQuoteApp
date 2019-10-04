<template>
  <div id="app">

    <Main/>

  </div>
</template>

<script>
import Main from './components/Main.vue'


export default {
  name: 'app',
  data() {
    return {

    }
  },
  components: {
    Main,
    
  }, 


}
</script>

<style>

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

</style>
