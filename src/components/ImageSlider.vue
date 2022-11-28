<template>
<Swiper 
    :modules="modules"
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 7500,
      disableOnInteraction: false,
    }"
    :pagination="{
      clickable: false,
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
            sub: "Magarita Pizza",
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
            sub: "Pepperoni Pizza",
            desciption: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt doloremque de',
            link: 'Order Now',
            img: 'https://galaxypizza.com.ng/wp-content/uploads/2018/05/PEPPERONI-PIZZA-03-e1643717811278.jpg'
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