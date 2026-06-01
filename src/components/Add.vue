<script>
export default{
    methods: {
        closeAdd(){
            this.$emit('closeModal')
        },
        add(){
            this.$emit('submitProduct', {name: this.brandName, image: this.newImage, price: this.Price})
        }
    },
    data() {
        return {
            brandName: '',
            newImage: '',
            Price: ''
        }
    },
}
</script>
<template>
    <div class="w-full h-screen bg-black/30 absolute top-0 z-50">
        <div class="flex justify-end mt-25 pr-40 absolute top-0 right-0">
            <div class="px-10 py-5 bg-amber-900 border rounded-xl">
                <h1 class="text-lg text-white mb-3">add a product/s</h1>
                <div class="flex flex-col">
                    <input v-model="newImage" class="px-3 py-2 rounded-xl text-white border-2 border-white outline-none" type="url" name="" id="" placeholder="Image Link">
                    <input v-model="brandName" class="px-3 py-2 rounded-xl text-white border-2 border-white my-4 outline-none" type="text" placeholder="Product Name">
                    <input v-model="Price" class="px-3 py-2 rounded-xl text-white border-2 border-white outline-none" type="number" placeholder="Product Price">
                    <div class="flex justify-center mt-2 flex-col">
                        <button class="px-10 py-2 rounded-full bg-amber-800/90 border-2 border-white text-white hover:scale-105 hover:shadow-xl/10 hover:shadow-white m-5 cursor-pointer" @click="add">Add</button>
                        <button class="text-lg font-semibold text-white cursor-pointer hover:underline" @click="closeAdd">Cancel</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>