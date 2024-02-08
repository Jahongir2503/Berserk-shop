<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import MainPage from '@/components/MainPage.vue';

export default {
  name: 'HomeView',
  components: {
    MainPage
  }
}
</script>
