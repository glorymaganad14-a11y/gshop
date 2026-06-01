<script>
export default {
    props: {
        cartitems: {
            type: Array
        }
    },
    methods: {
    },
}
</script>
<template>
    <div class="bg-amber-900/20">

        <div class="w-full h-auto">
        </div>
        <div class="bg-amber-900/60 h-auto py-5 ">

            <div class="flex justify-center mt-30">
                <div class="w-310 h-auto bg-white mt-5">
                    <div class="flex justify-between">
                        <h1 class="px-5 py-2 text-lg text-gray-400">Product</h1>
                        <div class="flex mx-10 items-center gap-30">
                            <h1 class="text-gray-400">Unit Price</h1>
                            <h1 class="text-gray-400">Quantity</h1>
                            <h1 class="text-gray-400">Total Price</h1>
                            <h1 class="text-gray-400">Actions</h1>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-10 flex justify-center">
                <div>
                    <div v-if="cartitems.length === 0">
                        <h1 class="text-2xl text-white">Your Cart is Empty</h1>
                    </div>
                </div>
                <div class="flex-col">
                    <div v-for="item in cartitems" class="gap-3 bg-white p-3 w-310 my-2">
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-10">
                                <img :src="item.image" alt="" class="w-20 h-20">
                                <h1 class="text-lg">{{ item.name }}</h1>
                            </div>
                            <div class="flex gap-27 ml-30">
                                <h1>₱{{ item.price }}</h1>
                                <h1 class="ml-8">1</h1>
                                <h1 class="ml-10 text-red-500 font-semibold">₱{{ item.price }}</h1>
                            </div>
                            <div>
                                <h1 class="mr-5 p-2 bg-blue-600 rounded-full text-white font-black">></h1>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div></div>
    </div>
</template>