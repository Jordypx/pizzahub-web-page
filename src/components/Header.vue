<template>
    <header class="fixed top-0 left-0 right-0 flex items-center justify-between">

       <div class="left-head flex items-center">
        <a href="#" class="logo text-4xl font-extrabold text-black flex"><ion-icon name="pizza" class="text-orange-600 mb-2"></ion-icon><p class="">pizzahub</p></a>

    <nav class="navbar">
    <!-- <a href="#home">Home</a>
    <a href="#dishes">dishes</a> -->
    <a href="#menu">Menu</a>
    <a href="#about">About</a>
    <a href="#reviews">reviews</a>
    <a href="#orders">orders</a>    
    </nav>
       </div>

    <div class="icons">
        <ion-icon name="menu-outline" class="menu cursor-pointer"></ion-icon>
        <ion-icon class="searcr cursor-pointer" name="search-outline"></ion-icon>
        <a class=" " href="#"><ion-icon name="heart"></ion-icon></a>
        <a class="" href="#"><ion-icon name="cart"></ion-icon></a>
    </div>
    
    </header>
</template>



<script>
export default {
    name: 'Header'
}
</script>