<template>
  <div>
    <Header />
    <Landing />
    <Features />
    <Screens1 />
    <Gallery />
    <Screens2  />
    <Feedback />
    <Subscribe />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Landing from './components/Landing.vue'
import Features from './components/Features.vue'
import Screens1 from './components/Screens1.vue'
import Gallery from './components/Gallery.vue'
import Screens2 from './components/Screens2.vue'
import Feedback from './components/Feedback.vue'
import Subscribe from './components/Subscribe.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Landing,
    Features,
    Screens1,
    Gallery,
    Screens2 ,
    Feedback,
    Subscribe,
    Footer
  }
}
</script>
