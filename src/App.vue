<template>
 <Header />
 <ImageSlider />
 <dishes />
</template>

<script>
import Header from './components/Header.vue'
import ImageSlider from './components/ImageSlider.vue'
import dishes from './components/dishes.vue'

export default {
  name: 'App',
  components: {
   Header,
   ImageSlider,
   dishes,
  }
}
</script>
 