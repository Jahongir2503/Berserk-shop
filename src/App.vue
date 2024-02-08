<template>
  <div>
    <Header/>
    <MainPage/>
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import MainPage from '@/components/MainPage.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: {
    Header,
    MainPage,
    Footer
  }
}
</script>