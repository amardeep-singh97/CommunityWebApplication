<template>
  <!-- <Header user_type="customer"></Header> -->
  <HeaderCustomer/>
  <section class="text-gray-600 body-font overflow-hidden">
    <div class="container px-5 pt-10 pb-5 mx-auto">
      <div class="lg:w-4/5 mx-auto flex flex-wrap">
        <div class="lg:w-1/2 w-full lg:pl-10 lg:py-6 mt-6 lg:mt-0">
          <h2 class="text-sm title-font text-gray-500 tracking-widest">FAST FOOD</h2>
<!--           <pre>{{ contents }}</pre>-->
<!--           <pre>{{ contentsList }}</pre>-->
          <h1 class="text-gray-900 text-3xl title-font font-medium mb-1 uppercase ">{{ contents.restaurant_name }}</h1>
          <div class="flex mb-4">
            <!-- Ratings -->
            <span class="flex items-center">
               <svg fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 text-yellow-500" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"></path>
               </svg>
               <svg fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 text-yellow-500" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"></path>
               </svg>
               <svg fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 text-yellow-500" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"></path>
               </svg>
               <svg fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 text-yellow-500" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"></path>
               </svg>
               <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 text-yellow-500" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"></path>
               </svg>
               <span class="text-gray-600 ml-3">4 Reviews</span>
            </span>
            <!-- Social media -->
            <!--          <span class="flex ml-3 pl-3 py-2 border-l-2 border-gray-200 space-x-2s">-->
            <!--            <a class="text-gray-500">-->
            <!--              <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">-->
            <!--                <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"></path>-->
            <!--              </svg>-->
            <!--            </a>-->
            <!--            <a class="text-gray-500">-->
            <!--              <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">-->
            <!--                <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"></path>-->
            <!--              </svg>-->
            <!--            </a>-->
            <!--            <a class="text-gray-500">-->
            <!--              <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">-->
            <!--                <path d="M21 11.5a8.38 8.38 0 01-.9 3.8 8.5 8.5 0 01-7.6 4.7 8.38 8.38 0 01-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 01-.9-3.8 8.5 8.5 0 014.7-7.6 8.38 8.38 0 013.8-.9h.5a8.48 8.48 0 018 8v.5z"></path>-->
            <!--              </svg>-->
            <!--            </a>-->
            <!--          </span>-->
          </div>
          <!-- Information of restaurant -->
          <p class="leading-relaxed">Food for us comes from our relatives, whether they have wings or fins or roots. That is how we consider food. Food has a culture. It has a history. It has a story. It has relationships.<br>
            <br><b>Address:</b> {{ contents.address1 }} {{ contents.address2}}, {{ contents.city}}, {{ contents.province}}, {{ contents.zip}}
          </p>
          <div class="flex mt-6 items-center pb-5 border-b-2 border-gray-100 mb-5">
            <div class="flex">
              <span class="mr-3">Closing Time:</span>
              <span class="mr-3">{{ contents.closes_at }}</span>
            </div>
          </div>
          <div class="flex">
            <span class="title-font font-medium text-2xl text-gray-900">+ {{ contents.phone }}</span>
            <!--          <button class="flex ml-auto text-white bg-yellow-500 border-0 py-2 px-6 focus:outline-none hover:bg-yellow-600 rounded">Call Restaurant</button>-->
            <!--          <button class="rounded-full w-10 h-10 bg-gray-200 p-0 border-0 inline-flex items-center justify-center text-gray-500 ml-4">-->
            <!--            <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">-->
            <!--              <path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"></path>-->
            <!--            </svg>-->
            <!--          </button>-->
          </div>
        </div>
        <!-- Restaurant Image -->
        <!-- <img alt="ecommerce" class="lg:w-1/2 w-full p-10 mx-auto lg:h-auto h-64 object-cover object-center rounded-full" src="https://source.unsplash.com/400x400/?food?sig-12"> -->
        <img class="img-fluid lg:w-1/2 w-full p-10 mx-auto lg:h-auto h-64 object-cover object-center rounded-full" :src="'data:image/jpg;base64,'+contents.picture" alt="" />
      </div>
    </div>
  </section>
  <!-- List of food items -->
  <div class="flex mt-6 items-center pb-5 border-b-2 border-gray-100 mb-5"></div>
  <div class="container mx-auto px-6">
    <h3 class="text-gray-700 text-2xl font-medium">List of food available</h3>
    <span class="mt-3 text-sm text-gray-500">{{length}} available</span>
    <div class="grid gap-6 grid-cols-1 sm:grid-cols-3 lg:grid-cols-5 xl:grid-cols-6 mt-6">
      <!-- Common restaurant card starts below -->
      <div v-for="content in contentsList" :key="content.foodDetailId" class="w-full max-w-sm mx-auto rounded-md shadow-md overflow-hidden">
        <!-- <div class="flex items-end justify-end h-56 w-full bg-cover image-holder"> -->
        <!-- <img class="img-fluid" :src="'data:image/jpg;base64,'+content.picture" alt="" /> -->
        <div class="flex h-56 md:h-44 w-full image-holder">
          <img v-if="content.picture" class="img-fluid object-cover" :src="'data:image/jpg;base64,'+content.picture" alt="" />
          <img v-else class="img-fluid" src="https://www.capitalcitysoulfood.com/Content/commerce-icons/menu-item-placeholder.png" alt="" />
        </div>
        <div class="px-5 py-3">
          <h3 class="text-gray-700 uppercase">{{ content.itemName }}</h3>
          <span class="text-gray-400 mt-2">Quantity: {{ content.numberofPackets }}</span>
          <div v-if="content.numberofPackets > 0">
            <button class="block w-full mt-3 text-white bg-yellow-500 py-2 px-4 focus:outline-none hover:bg-yellow-600 rounded-md" @click="claimItem(content.foodDetailId, content.id)">
              Claim This Item
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <claim-food-modal v-if="claimModalVisible" @close="claimModalVisible = false" :food-id="foodId" :restaurant-id="restaurantId"></claim-food-modal>
  <Footer/>
</template>
<script>
import HeaderCustomer from "@/components/HeaderCustomer.vue";
import Footer from "@/components/Footer.vue";
import axios from 'axios'
import {path} from './settings.js'
import ClaimFoodModal from "@/components/food/ClaimFoodModal";

export default
{
  name: "RestaurantProfile",
  props: ['id'],
  data() {
    return {
      foodId: null,
      restaurantId: null,
      contents: [],
      contentsList: null,
      length: null,
      claimModalVisible: false
    }
  },
  created() {
    const token = localStorage.getItem("token");
    axios({
      url: path + '/profile/'+this.id,
      method: "POST",
      headers: {
        Authorization: `Bearer ${token}`,
        "Access-Control-Allow-Origin": "*",
        "Content-type": "application/json",
      },
      data : this.user
    }).then((response) => {
      this.contents = response.data[0]
      console.log(this.contents)
    }, (error) => {
      console.log(error);
    });

    axios({
      url: path + '/restaurant/'+this.id,
      method: "POST",
      headers: {
        Authorization: `Bearer ${token}`,
        "Access-Control-Allow-Origin": "*",
        "Content-type": "application/json",
        
      },
      data : this.user
    }).then((response) => {
      this.contentsList = response.data
      this.length = response.data.length
      console.log(this.length)

    }, (error) => {
      console.log(error);
    });
  },
  methods: {
    claimItem: function (foodId, restaurantId) {
      this.foodId = foodId
      this.restaurantId = restaurantId
      this.claimModalVisible = true
    }
  },
  components: {
    HeaderCustomer,
    Footer,
    ClaimFoodModal
  },
};
</script>
<style scoped></style>