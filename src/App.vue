<script>
import AppHeader from './components/AppHeader.vue';

export default{
  data() {
    return{

    }
  },
  components: 
  {AppHeader},
}
</script>

<template>
  <h1>Hello</h1>
  <AppHeader/>
  <router-view></router-view>
</template>

<style lang="scss">
@use "./styles/general.scss" as *
</style>