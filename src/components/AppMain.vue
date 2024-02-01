<script>
import axios from 'axios';

export default{
  data() {
    return{

    }
  },
  created(){
    axios.get('http://127.0.0.1:8000/api/projects')
    .then((resp) => {
        console.log(resp);
        
    })

  }
}

</script>

<template>
  <h1>Main</h1>
</template>

<style lang="scss" scoped>

</style>