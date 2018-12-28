<template>
  <div id="app">
    <Header/>
    <Skill/>
    <Experience/>
    <Portfolio/>
    <Education/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Skill from './components/Skill.vue'
import Experience from './components/Experience.vue'
import Portfolio from './components/Portfolio.vue'
import Education from './components/Education.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    Header,
    Skill,
    Experience,
    Portfolio,
    Education,
    Footer,
  }
}
</script>
