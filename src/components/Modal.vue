<script>
export default {
    props: {
        selectedProduct: {
            type: Object,
        }
    }, methods:
    {
        closeModal() {
            this.$emit('CancelModal')
        },
        confirmAdd() {
            this.$emit('addtocart', this.selectedProduct)
        }
    }
}
</script>
<template>
    <div class="bg-black/40 w-full h-screen fixed top-20 z-40">
        <div class="flex justify-center bg-black/10 w-full h-auto">
            <div class="w-200 h-auto rounded-xl bg-white absolute top-30">
                <div>

                </div>
                <div class="flex">
                    <img class="w-100 h-90" :src="selectedProduct.image" alt="">
                    <div>
                        <div class="px-5">
                            <h1 class="text-amber-900 text-2xl mt-10 font-bold">{{ selectedProduct.name }}</h1>
                            <h3 class="text-red-600 text-xl bg-amber-900/10 py-3 px-3">${{ selectedProduct.price }}.00</h3>
                        </div>
                        <div class="flex mt-5 px-5">
                            <svg class="w-6 h-6 text-yellow-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                                width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                                <path
                                    d="M13.849 4.22c-.684-1.626-3.014-1.626-3.698 0L8.397 8.387l-4.552.361c-1.775.14-2.495 2.331-1.142 3.477l3.468 2.937-1.06 4.392c-.413 1.713 1.472 3.067 2.992 2.149L12 19.35l3.897 2.354c1.52.918 3.405-.436 2.992-2.15l-1.06-4.39 3.468-2.938c1.353-1.146.633-3.336-1.142-3.477l-4.552-.36-1.754-4.17Z" />
                            </svg>
                            <svg class="w-6 h-6 text-yellow-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                                width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                                <path
                                    d="M13.849 4.22c-.684-1.626-3.014-1.626-3.698 0L8.397 8.387l-4.552.361c-1.775.14-2.495 2.331-1.142 3.477l3.468 2.937-1.06 4.392c-.413 1.713 1.472 3.067 2.992 2.149L12 19.35l3.897 2.354c1.52.918 3.405-.436 2.992-2.15l-1.06-4.39 3.468-2.938c1.353-1.146.633-3.336-1.142-3.477l-4.552-.36-1.754-4.17Z" />
                            </svg>
                            <svg class="w-6 h-6 text-yellow-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                                width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                                <path
                                    d="M13.849 4.22c-.684-1.626-3.014-1.626-3.698 0L8.397 8.387l-4.552.361c-1.775.14-2.495 2.331-1.142 3.477l3.468 2.937-1.06 4.392c-.413 1.713 1.472 3.067 2.992 2.149L12 19.35l3.897 2.354c1.52.918 3.405-.436 2.992-2.15l-1.06-4.39 3.468-2.938c1.353-1.146.633-3.336-1.142-3.477l-4.552-.36-1.754-4.17Z" />
                            </svg>
                            <svg class="w-6 h-6 text-yellow-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                                width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                                <path
                                    d="M13.849 4.22c-.684-1.626-3.014-1.626-3.698 0L8.397 8.387l-4.552.361c-1.775.14-2.495 2.331-1.142 3.477l3.468 2.937-1.06 4.392c-.413 1.713 1.472 3.067 2.992 2.149L12 19.35l3.897 2.354c1.52.918 3.405-.436 2.992-2.15l-1.06-4.39 3.468-2.938c1.353-1.146.633-3.336-1.142-3.477l-4.552-.36-1.754-4.17Z" />
                            </svg>
                            <svg class="w-6 h-6 text-yellow-500" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                                width="24" height="24" fill="none" viewBox="0 0 24 24">
                                <path stroke="currentColor" stroke-width="2"
                                    d="M11.083 5.104c.35-.8 1.485-.8 1.834 0l1.752 4.022a1 1 0 0 0 .84.597l4.463.342c.9.069 1.255 1.2.556 1.771l-3.33 2.723a1 1 0 0 0-.337 1.016l1.03 4.119c.214.858-.71 1.552-1.474 1.106l-3.913-2.281a1 1 0 0 0-1.008 0L7.583 20.8c-.764.446-1.688-.248-1.474-1.106l1.03-4.119A1 1 0 0 0 6.8 14.56l-3.33-2.723c-.698-.571-.342-1.702.557-1.771l4.462-.342a1 1 0 0 0 .84-.597l1.753-4.022Z" />
                            </svg>
                            <h1>5.9</h1>
                        </div>
                        <div class="px-5 pt-3">
                            <h3 class="text-sm">Shop Vouchers: <span class="bg-red-500/50 px-3 py-1 rounded-lg">15% OFF</span></h3>
                            <h3 class="text-sm">Shipping: <span class="font-semibold text-amber-800">Pre Order (ships in 30 days)</span></h3>
                            <h3 class="text-sm">Shopping Guarantee: 100% Authentic • Free & Easy Returns • Merchandise Protection</h3>
                            <h3 class="text-base text-gray-400 underline">review comments</h3>
                        </div>
                        <div class="flex gap-3 mt-5 px-5">
                            <button @click="confirmAdd"
                            class="px-10 bg-amber-900 text-white rounded-xl hover:bg-amber-800 cursor-pointer">confirm</button>
                            <button @click="closeModal"
                            class="px-11 py-1 bg-red-600 text-white rounded-xl hover:bg-red-500 cursor-pointer">cancel</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>