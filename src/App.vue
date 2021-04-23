<template>
  <v-app>
    <HeaderID />
    <v-main>
     <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import HeaderID from './components/HeaderID';

export default {
  name: 'App',

  components: {
    HeaderID,
  },

  data() {
    return {
        
    }
  }
};
</script>

<style scoped>
#app {
    background-color:#272727;
}


</style>
