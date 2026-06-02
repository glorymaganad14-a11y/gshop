<script>
export default {
    props: {
        cartitems: {
            type: Array
        }
    },
    methods: {
        checkOut() {
            this.$emit('purchase', this.cartitems)
        },
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
                        <h1 class="px-5 py-2 text-lg text-gray-400 cursor-pointer hover:text-amber-800">Product</h1>
                        <div class="flex mx-10 items-center gap-35 mr-15">
                            <h1 class="text-gray-400 cursor-pointer hover:text-amber-800">Unit Price</h1>
                            <h1 class="text-gray-400 cursor-pointer hover:text-amber-800">Quantity</h1>
                            <h1 class="text-gray-400 cursor-pointer hover:text-amber-800">Total Price</h1>
                            <h1 class="text-gray-400 cursor-pointer hover:text-amber-800">Actions</h1>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-10 flex justify-center">
                <div>
                    <div v-if="cartitems.length === 0">
                        <div class="flex flex-col justify-center">
                            <img class="w-50 rounded-full border-4 border-white"
                                src="https://i.pinimg.com/736x/8e/0c/35/8e0c35603c6c3a228065cc472a8a02a7.jpg" alt="">
                            <h1 class="text-2xl text-white font-black">Your Cart is Empty</h1>
                        </div>
                    </div>
                </div>
                <div class="flex-col">
                    <div v-for="item in cartitems" class="gap-3 bg-white p-3 w-310 my-2">
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-10">
                                <img :src="item.image" alt="" class="w-20 h-20">
                                <h1 class="text-lg">{{ item.name }}</h1>
                            </div>
                            <div class="flex gap-30 ml-30">
                                <h1>₱{{ item.price }}</h1>
                                <h1 class="ml-8">1</h1>
                                <h1 class="ml-10 text-red-500 font-semibold">₱{{ item.price }}</h1>
                            </div>
                            <div class="mr-5">
                                <h1 @click="checkOut"
                                    class=" px-2 py-1 bg-amber-900 rounded-full text-white cursor-pointer hover:bg-amber-900/80">
                                    check out</h1>
                                <h1 class="text-center text-red-500 cursor-pointer hover:underline">delete</h1>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div>
                <div class="flex justify-center mt-20">
                    <div class="w-310 h-auto p-4 bg-white border-b-5 border-amber-900">
                        <h1 class="text-lg text-gray-500">YOU MAY ALSO LIKE</h1>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>