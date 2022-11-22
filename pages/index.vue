<template>
  <div class="main-content">
    <Nav />
    <Header />
    <Employees v-for="(dataInfo,id) in employees" :key='id' :cardInfo="dataInfo"/>
    <Footer />
  </div>
</template>

<script>
import Nav from '../components/Nav.vue'
import Footer from '../components/Footer.vue'
import Header from '../components/Header.vue'
import Employees from '../components/Employees.vue'
import employees from '../assets/data.js'
export default {
  name: 'IndexPage',
  components: {
    Nav,
    Footer,
    Header,
    Employees,
  },
  data() {
    return {
       employees,
    }
  },
  head() {
    return {
      title: 'Home',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Home View',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>