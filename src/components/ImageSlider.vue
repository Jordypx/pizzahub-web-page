<template>
<Swiper 
    :modules="modules"
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 7500,
      disableOnInteraction: false,
    }"
   
   >

   <swiper-slide v-for="text in swiperTextBase" :key="text.id" class="home">
      <div class="home-slider">
         <div class="wrapper">
            <div class="slide">
             <div class="content">
              <span>{{ text.head }}</span>
               <h3>{{ text.sub }}</h3>
                <P>{{ text.desciption }}</P>
                <a class="btn" href="#">{{ text.link }}</a>
          </div>

      <div class="image">
         <img :src="text.img" alt="image">
      </div>
      </div>
         </div>
      </div>
   </swiper-slide>

</Swiper>
</template>





<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/pagination";

// import {ref} from 'vue'

import { Autoplay, Pagination } from "swiper";

export default {

   name: 'ImageSlider',

   components: {
    Swiper,
    SwiperSlide,
  },

   data() {
      return {
         swiperTextBase:[
         {
            id: "1",
            head: 'Our special menu',
            sub: "cheese Pizza",
            desciption: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt doloremque de',
            link: 'Order Now',
            img: 'https://eatcaulipower.com/assets/images/products/_detail/854934007099_product_2022-07-25-230439_lmae.jpg'
         },
         {
            id: "2",
            head: 'Our special menu',
            sub: "Chicken Pizza",
            desciption: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt doloremque de',
            link: 'Order Now',
            img: 'https://www.innit.com/meal-service/en-US/images/Meal-Pizza%3A%20Premade_Crust-Hawaiian_BBQ_Chicken_1533765621645_640x640.png'
         },
         {
            id: "3",
            head: 'Our special menu',
            sub: "beef Pizza",
            desciption: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt doloremque de',
            link: 'Order Now',
            img: 'https://0bb8856ba8259ec33e3d-a40599a114f3a4c6d0979c3ffe0b2bf5.ssl.cf2.rackcdn.com/0287525000000_CL_hyvee_default_large.jpeg'
         },
      ]
      }
   },

   setup() {
      
      return {
         modules: [Autoplay, Pagination]
      }
   },

}

</script>