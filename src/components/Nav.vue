<script>
export default {
    data() {
        return {
            searchbar: ''
        }
    },
    methods: {
        addModal() {
            this.$emit('OpenAddModal')
        },
        navigate(page) {
            this.$emit('goTo', page)
        },
        search() {
            this.$emit('searchBar', this.searchbar)
        }
    },
}
</script>
<template>
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
                    <input v-model="searchbar" @input="search" class="w-220 bg-white px-3 py-2 rounded outline-none"
                        type="text" placeholder="Back To School Deals">

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
                <div class="flex gap-2">
                    <svg @click="navigate('showCart')"
                        class="w-12 h-12 text-amber-900 cursor-pointer p-2 bg-white rounded-full" aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm-8.5-3h9.25L19 7H7.312" />
                    </svg>
                    <svg @click="navigate('history')"
                        class="w-12 h-12 text-amber-900 cursor-pointer p-2 bg-white rounded-full" aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                        viewBox="0 0 24 24">
                        <path fill-rule="evenodd"
                            d="M14 7h-4v3a1 1 0 0 1-2 0V7H6a1 1 0 0 0-.997.923l-.917 11.924A2 2 0 0 0 6.08 22h11.84a2 2 0 0 0 1.994-2.153l-.917-11.924A1 1 0 0 0 18 7h-2v3a1 1 0 1 1-2 0V7Zm-2-3a2 2 0 0 0-2 2v1H8V6a4 4 0 0 1 8 0v1h-2V6a2 2 0 0 0-2-2Z"
                            clip-rule="evenodd" />
                    </svg>
                    <svg class="w-12 h-12 text-amber-900 cursor-pointer p-2 bg-white rounded-full" aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M12 21a9 9 0 1 0 0-18 9 9 0 0 0 0 18Zm0 0a8.949 8.949 0 0 0 4.951-1.488A3.987 3.987 0 0 0 13 16h-2a3.987 3.987 0 0 0-3.951 3.512A8.948 8.948 0 0 0 12 21Zm3-11a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
                    </svg>

                </div>

            </div>
        </div>
    </nav>
</template>