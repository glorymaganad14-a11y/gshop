<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        addModal() {
            this.$emit('OpenAddModal')
        },
        navigate(page) {
            this.$emit('goTo', page)
        }
    },
}
</script>
<template>
    <!-- <header
        class="fixed inset-x-0 top-0 z-30 mx-auto w-full border border-gray-100 bg-white/80 py-3 shadow backdrop-blur-lg md:top-6 md:rounded-3xl lg:max-w-5xl">
        <div class="px-4">
            <div class="flex items-center justify-between">
                <div class="flex shrink-0">
                    <a aria-current="page" class="flex items-center" href="/">
                        <img class="h-10 0w-auto"
                            src="../assets/images/cat.png" alt="">
                        <p class="sr-only">Website Title</p>
                    </a>

                </div>
                <div class="hidden md:flex md:items-center md:justify-center md:gap-5">
                    <a aria-current="page" @click="navigate('home')"
                        class="inline-block rounded-lg px-2 py-1 text-sm font-medium text-gray-900 transition-all duration-200 hover:bg-gray-100 hover:text-gray-900"
                        href="#">Home</a>
                    <a class="inline-block rounded-lg px-2 py-1 text-sm font-medium text-gray-900 transition-all duration-200 hover:bg-gray-100 hover:text-gray-900"
                        href="#">Products</a>
                    <a class="inline-block rounded-lg px-2 py-1 text-sm font-medium text-gray-900 transition-all duration-200 hover:bg-gray-100 hover:text-gray-900"
                        href="#">Services</a>
                </div>
                <div class="flex items-center justify-end gap-3">
                    <a class="hidden items-center justify-center rounded-xl bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 transition-all duration-150 hover:bg-gray-50 sm:inline-flex"
                        href="/login">Sign in</a>
                    <a class="inline-flex items-center justify-center rounded-xl bg-amber-900 px-3 py-2 text-sm text-white font-semibold shadow-sm transition-all duration-150 hover:bg-amber-800 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600"
                        href="/login">Login</a>
                    <p @click="addModal"
                        class="inline-flex items-center justify-center rounded-xl bg-amber-900 px-3 py-2 text-sm text-white font-semibold shadow-sm transition-all duration-150 hover:bg-amber-800 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600 cursor-pointer">
                        Add</p>
                    <svg @click="navigate('showCart')"
                        class="w-12 h-12 text-white p-1 bg-amber-900 rounded-full cursor-pointer hover:bg-amber-800"
                        aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none"
                        viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7H7.312" />
                    </svg>
                    <span class="bg-red-600 w-5 h-5 rounded-full absolute top-2"></span>
                </div>
            </div>
        </div>
    </header> -->
    <nav class="fixed w-full z-50">
        <div class="w-full bg-amber-900/80 h-auto backdrop-blur-lg">
            <div class="flex justify-around">
                <div class="flex gap-5 text-white/90 text-sm mt-2">
                    <h1 class="hover:bg-white/40 hover:border-lg cursor-pointer hover:px-2">Seller Centre</h1>
                    <h1 class="hover:bg-white/40 hover:border-lg cursor-pointer hover:px-2">start Selling</h1>
                    <h1 class="hover:bg-white/40 hover:border-lg cursor-pointer hover:px-2">Download</h1>
                    <h1 class="hover:bg-white/40 hover:border-lg cursor-pointer hover:px-2">Follow us on</h1>
                </div>
                <div class="flex gap-5 text-white text-sm mt-2">
                    <h1 class="cursor-pointer hover:bg-white/50 ">Notification</h1>
                    <h1 class="cursor-pointer hover:bg-white/50  ">Help</h1>
                    <h1 class="cursor-pointer hover:bg-white/50  ">English</h1>
                    <h1 class="cursor-pointer hover:bg-white/50  ">User</h1>
                </div>
            </div>
            <div class="flex justify-center items-center gap-15 mt-3">
                <img class="w-20 rounded-full mb-5" @click="navigate('home')"
                    src="https://i.pinimg.com/1200x/7b/aa/d5/7baad582f590bedbddbdadcd53634bca.jpg" alt="">
                <div class="flex flex-col gap-2">
                    <input class="w-220 bg-white px-3 py-2 rounded outline-none" type="text" placeholder="Back To School Deals">

                    <div class="flex gap-2 text-[13px] text-white/90 font-lighter">
                        <span class="cursor-pointer hover:bg-white/70">Lovito Top</span>
                        <span class="cursor-pointer hover:bg-white/70">Shoes for Women</span>
                        <span class="cursor-pointer hover:bg-white/70">Lovito Summer Outfit For Women</span>
                        <span class="cursor-pointer hover:bg-white/70">Lovito Sleeveless Tops</span>
                        <span class="cursor-pointer hover:bg-white/70">Downtown Clothes</span>
                        <span class="cursor-pointer hover:bg-white/70">Denim Short Skirt</span>
                        <span class="cursor-pointer hover:bg-white/70">Coral Daisy Bag</span>
                    </div>
                </div>
                <svg @click="navigate('showCart')" class="w-15 h-15 text-amber-900 cursor-pointer p-2 bg-white rounded-full" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                    width="24" height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7H7.312" />
                </svg>
            </div>
        </div>
    </nav>
</template>