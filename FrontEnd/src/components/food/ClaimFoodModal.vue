<template>
  <transition name="modal-fade">
      <div class="modal-backdrop" role="dialog">
        <div class="flex items-center justify-center fixed left-0 bottom-0 w-full h-full">
          <div class="bg-white rounded-lg w-11/12 md:w-1/4">
            <div class="flex flex-col items-start p-4">
              <div class="flex items-center w-full">
                <div class="text-gray-900 font-medium text-lg">Are you sure you want to claim this item?</div>
                <svg class="ml-auto fill-current text-gray-700 w-6 h-6 cursor-pointer" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18 18" @click="close" aria-label="Close modal">
                  <path d="M14.53 4.53l-1.06-1.06L9 7.94 4.53 3.47 3.47 4.53 7.94 9l-4.47 4.47 1.06 1.06L9 10.06l4.47 4.47 1.06-1.06L10.06 9z"/>
                </svg>
              </div>
              <div class="ml-auto space-x-2 mt-6">
                <button type="button" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="claimItem()">
                  Yes
                </button>
                <button class="bg-transparent hover:bg-gray-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded" @click="close" aria-label="Close modal">
                  No
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
  </transition>
</template>

<script>
import axios from "axios";
import {path} from '@/views/settings'
export default {
  name: "ClaimFoodModal",
  props: {
    foodId: Number,
    restaurantId: Number
  },
  methods: {
    close: function() {
      this.$emit('close');
    },
    claimItem: function () {
      console.log(this.foodId)
      console.log(this.restaurantId)
      const token = localStorage.getItem("token");
      // axios.post(path + '/customer/claim-food', {
      //   foodId: this.foodId,
      //   restaurantId: this.restaurantId,
      // })
      
      axios({
      url: path + "/customer/claim-food",
      method: "POST",
      headers: {
        Authorization: `Bearer ${token}`,
        "Access-Control-Allow-Origin": "*",
        "Content-type": "application/json",
      },
     data: {
      foodId: this.foodId,
      restaurantId: this.restaurantId
      },
    }).then(response => {
        this.$emit('close');
      }).catch(error => {
        console.log(error)
      })
    }
  }
}
</script>

<style scoped>

</style>