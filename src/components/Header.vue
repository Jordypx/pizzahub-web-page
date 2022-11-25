<template>
    <header class="fixed top-0 left-0 right-0 flex items-center justify-between">

       <div class="left-head flex items-center">
        <a href="#" class="logo text-4xl font-extrabold text-black flex"><ion-icon name="pizza" class="text-orange-600 mb-2"></ion-icon><p class="">pizzahub</p></a>
 
    <nav class="navbar">
    <!-- <a href="#home">Home</a>
    <a href="#dishes">dishes</a> -->
     
    <ion-icon @click="CloseClick" class="close-menu" name="close"></ion-icon>

    <a href="#menu">Menu</a>
    <a href="#about">About</a>
    <a href="#reviews">reviews</a>
    <a href="#orders">orders</a>    
    </nav>
       </div>

    <div class="icons">
        <ion-icon @click="OnClick" name="menu-outline" class="menu cursor-pointer"></ion-icon>
        <ion-icon class="search cursor-pointer" name="search-outline"  @click="onSearch"></ion-icon>
        <a class=" " href="#"><ion-icon name="heart"></ion-icon></a>
        <a class="" href="#"><ion-icon name="cart"></ion-icon></a>
    </div>
    </header>

    <form action="" class="search-form fixed top-0 left-0 h-full w-full">

      <div class="lightbox flex items-center justify-center">
        <input type="search" placeholder="Search here..." name="" id="" class="search-box">
        <label class="text-white cursor-pointer text-4xl" for="search-box"><ion-icon class="w-16 h-16" name="search-sharp"></ion-icon></label>
      </div>

        <ion-icon @click="onCloseClick" class="close absolute text-white cursor-pointer top-8 right-12 text-7xl" name="close"></ion-icon>
    </form>
</template>



<script>


export default {
    name: 'Header',

    components : {
    },

    methods: {
        OnClick() {
         document.querySelector('.navbar').style.display= 'block'
        },

        CloseClick() {
            document.querySelector('.navbar').style.display= 'none'
        },

        onSearch () {
            document.querySelector('.search-form').style.display ='inline-block'
        },
       
        onCloseClick() {
        document.querySelector('.search-form').style.display ='none'
        // document.querySelector('.close').style.display ='none'
        }
    }

}





</script>