<script>
export default {
props: {
    purchased:{
        type: Array
    }
},
methods: {
    // checkOut(){
    //     this.$emit('clickCheckout')
    // }
},
}
</script>
<template>
    <div>
        <div class="bg-amber-800/40 w-full h-screen">
            <h1 class="text-2xl text-white font-semibold p-10 pl-35 pt-50">MY PURCHASE</h1>
            <div class="flex justify-center">
                <div class="w-310 bg-white h-auto p-2 flex justify-around border-t-10 border-amber-900">
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800 hover:border-b-3 hover:border-amber-900">All</h1>
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800">To Pay</h1>
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800">To Ship</h1>
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800">To Received</h1>
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800">Completed</h1>
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800">Cancelled</h1>
                    <h1 class="text-base text-gray-500 cursor-pointer hover:text-amber-800">Return Refund</h1>
                </div>
            </div>
            <!-- <div v-if="">
            </div> -->
            <div class="flex justify-center pt-10">
                <div></div>
                <div v-for="purchase in purchased" class="w-310 bg-white p-2 rounded-b-xl">
                    <div class="flex items-center justify-between px-5 py-3">
                        <div class="flex items-center gap-5">
                            <img class="w-20" :src="purchase.image" alt="">
                            <h1 class="text-xl font-semibold text-gray-700">{{ purchase.name }}name</h1>
                        </div>
                        <h2 class="text-red-500 text-lg">₱{{ purchase.price }}</h2>
                    </div>
                </div>
            </div>
            <div class="flex justify-center">
                <div class="w-310 bg-white ht-auto p-2 pb-5 border-t-2 border-dashed border-gray-400 rounded-t-lg flex justify-end">
                    <div>
                        <div class="flex justify-end pb-5 px-5">
                            <h1 class="text-base text-gray-600">Order Total: <span class="text-red-600 text-2xl font-semibold">₱</span></h1>
                        </div>
                        <div class="flex gap-5 px-5">
                            <button class="p-3 bg-amber-900 text-white cursor-pointer hover:bg-amber-800 text-sm rounded">RECEIVED</button>
                            <button class="p-2 border border-gray-400 cursor-pointer hover:bg-gray-200 text-sm text-gray-700">Request for Return/Refund</button>
                            <button class="p-2 border border-gray-400 cursor-pointer hover:bg-gray-200 text-sm text-gray-700">More</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>