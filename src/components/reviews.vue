<template>

    <div class="review">
       <h3 class="sub-heading"> customer's review</h3>
       <h1 class="heading"> what they say</h1>
    

    <Swiper 
    :slidesPerView="1"
    :modules="modules"
    :spaceBetween="20"
    :autoplay="{
      delay: 7500,
      disableOnInteraction: false,
    }"
    :pagination="{
      clickable: true,
    }"
    :breakpoints="{
      '0': {
        slidesPerView: 1,
        spaceBetween: 10,
      },
      '640': {
        slidesPerView: 2,
        spaceBetween: 20,
      },
      '768': {
        slidesPerView: 2,
        spaceBetween: 40,
      },
      '1024': {
        slidesPerView: 3,
        spaceBetween: 50,
      },
    }"
   class="swiper"
   >

   <swiper-slide v-for="text in swiperText" :key="text.id" class="swiper-slide">
     
    <div class="wrappers">
        <div class="slides">
            <div class="user">
                <img :src="text.img" alt="images">
                <div class="user-info">
                    <h3>{{ text.name }}</h3>
                <div class="stars">
                <ion-icon name="star"></ion-icon>
                <ion-icon name="star"></ion-icon>
                <ion-icon name="star"></ion-icon>
                <ion-icon name="star"></ion-icon>
                <ion-icon name="star-half"></ion-icon>
            </div>
                </div>
            </div>
            <p>{{ text.para }}</p>
        </div>
    </div>

   </swiper-slide>
</Swiper>
</div>
</template>





<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/pagination";

// import {ref} from 'vue'

import { Autoplay, Pagination } from "swiper";

export default {
    name: 'reviews',

    components: {
    Swiper,
    SwiperSlide,
  },

  data() {
    return {
        swiperText: [
            {
                id: "1",
                name: "sarah stone",
                para: "This resaurant is undeniably a five star restaurant I advice any person should try this cause it has become one of my favourite pizza places to go to.",
                img: "https://media.istockphoto.com/id/1386479313/photo/happy-millennial-afro-american-business-woman-posing-isolated-on-white.jpg?s=170667a&w=0&k=20&c=yJI4R1SULPnrLj1sxEwxfMaA7CUndElkyd9DHkoAJ1U="
            },
            {
                id: "2",
                name: "john deo",
                para: "This resaurant is undeniably a five star restaurant I advice any person should try this cause it has become one of my favourite pizza places to go to.",
                img: "https://media.istockphoto.com/id/1300972574/photo/millennial-male-team-leader-organize-virtual-workshop-with-employees-online.jpg?s=170667a&w=0&k=20&c=S9AVbcsSpY1e6vwbnrrZHJzlAtnuSQKtmk11fDItSHE="
            },
            {
                id: "3",
                name: "michael son",
                para: "This resaurant is undeniably a five star restaurant I advice any person should try this cause it has become one of my favourite pizza places to go to.",
                img: "https://media.istockphoto.com/id/1381221247/photo/beautiful-afro-girl-with-curly-hairstyle.jpg?b=1&s=170667a&w=0&k=20&c=0x91osZOkL8EfhTEEGNa2EeCGN2gdMTNULOsUFW_0i4="
            },
            {
                id: "4",
                name: "jamal lyon",
                para: "This resaurant is undeniably a five star restaurant I advice any person should try this cause it has become one of my favourite pizza places to go to.",
                img: "https://media.istockphoto.com/id/1338134336/photo/headshot-portrait-african-30s-man-smile-look-at-camera.jpg?b=1&s=170667a&w=0&k=20&c=j-oMdWCMLx5rIx-_W33o3q3aW9CiAWEvv9XrJQ3fTMU="
            },
        ]
    }
  },








  setup() {
      
      return {
         modules: [ Autoplay, Pagination]
      }
   },
}
</script>