<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <JumboTron msg="Metrobike Share"/>
    <SampleRow row_id="sample_row_1" col_id="sample_col_1" div_id="sample_div_1" json_file="bars.json" />
    <SampleRow row_id="sample_row_2" col_id="sample_col_2" div_id="sample_div_2" json_file="bars.json" />
    <SampleRow row_id="sample_row_3" col_id="sample_col_3" div_id="sample_div_3" json_file="bars.json" />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import JumboTron from './components/JumboTron.vue'
import SampleRow from './components/SampleRow.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld
    JumboTron,
    SampleRow
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
