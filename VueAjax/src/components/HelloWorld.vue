<template>
  <div class="hello">
      {{jsonData}}
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      jsonData:[]
    }
  },
  created() {
    let url = 'https://api.myjson.com/bins/19gaco' 
    axios.get(url).then((res) => {
        this.jsonData = res.data
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  width:600px;
  height:200px;
  margin:0 auto;
  border:1px solid #d3d3d3;
}
</style>
