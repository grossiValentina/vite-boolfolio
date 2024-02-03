<script>
import AppMain from './components/AppMain.vue'
import AppHeader from './components/AppHeader.vue';

export default{
  data() {
    return{

    }
  },
  components: 
  {AppMain, AppHeader},
}
</script>

<template>
  <h1>Hello</h1>
  <AppHeader/>
  <AppMain/>
  <!--<router-view/><router-view/>-->
</template>

<style lang="scss">
@use "./styles/general.scss" as *
</style>