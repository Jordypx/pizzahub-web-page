<template>
 <Header />
 <ImageSlider />
 <dishes />
 <About />
 <reviews />
</template>

<script>
import Header from './components/Header.vue'
import ImageSlider from './components/ImageSlider.vue'
import dishes from './components/dishes.vue'
import About from './components/About.vue'
import reviews from './components/reviews.vue'

export default {
  name: 'App',
  components: {
   Header,
   ImageSlider,
   dishes,
   About,
  reviews
  }
}
</script>
 