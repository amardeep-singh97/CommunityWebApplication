<template>
  <header class="text-gray-600 body-font">
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <router-link to="/" class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
        <img src="..\assets\images\logo.png" alt="" class="w-36">
      </router-link>
      <nav class=" md:mr-auto md:ml-4 md:py-1 md:pl-4 md:border-l md:border-gray-400 flex flex-wrap items-center text-base justify-center">
        <!-- <a class="mr-5 hover:text-gray-900 cursor-pointer">Home Page</a> -->
        <!-- <router-link class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/" exact>Home Page</router-link> -->
        <router-link  class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/customer/orders" exact>My Orders</router-link>
         <router-link  class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/restaurant" exact>Restaurants</router-link>
       
        <!-- <router-link v-if="user_type === 'customer'" class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/customer/orders" exact>My Orders</router-link> -->
        <!-- <router-link v-if="user_type === 'restaurant'" class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/restaurant/scan-qr-code" exact>Scan QR Code</router-link> -->
<!--        <router-link tag="li" class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/list" exact>Restaurant List</router-link>-->

        <!-- <a class="mr-5 hover:text-gray-900 cursor-pointer">About Us</a> -->
        <!-- <a class="mr-5 hover:text-gray-900 cursor-pointer">Contact Us</a> -->
        <!-- <router-link tag="li" class="mr-5 hover:text-gray-900 cursor-pointer" class-active="active" to="/ContactUs" exact>Contact Us</router-link> -->
      </nav>

      <!-- <router-link to="/sign-up" v-if="user_type !== 'restaurant' && user_type !== 'customer'">
        <button class=" inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0">
          Sign Up Now
          <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24" >
            <path d="M5 12h14M12 5l7 7-7 7"></path>
          </svg>
        </button> -->
      <router-link to ="/"> 
         <button  v-on:click="ClearCookies" class="inline-flex text-white bg-yellow-500 border-0 py-2 px-6 focus:outline-none hover:bg-yellow-600 rounded text-lg" >
          Sign out
           <svg fill="none"  class="w-4 h-4 ml-1" viewBox="0 0 24 24" >
            <path d="M5 12h14M12 5l7 7-7 7"></path>
          </svg>
        </button> 
        </router-link >
    </div>
  </header>
</template>

<script>

import axios from 'axios';
  export default {
    name: "HeaderCustomer",
    props: [
      'user_type'
    ],
    created() {

    },

   methods: {
    ClearCookies: function () {
    localStorage.removeItem('token');
    },
   }
  }
</script>