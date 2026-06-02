<script>
import Modal from './Modal.vue';
import Add from './Add.vue';
export default {
    props: {
        addingProduct: {
            type: Boolean
        },
        forSearch: {
            type: String
        }
    },
    components: {
        Modal,
        Add,
    },
    data() {
        return {
            products: [
                {
                    id: 1,
                    image: 'https://i.pinimg.com/736x/f4/bd/db/f4bddb8a36ad0fb2cf6a2cc6eed52d59.jpg',
                    name: 'Classy Bag',
                    price: '400',
                },
                {
                    id: 2,
                    image: 'https://i.pinimg.com/736x/55/c8/46/55c846c5959f53cb951de7324419c62c.jpg',
                    name: 'Headphone',
                    price: '341',
                },
                {
                    id: 3,
                    image: 'https://i.pinimg.com/1200x/db/86/06/db8606b583230d321268cfd7877bd55b.jpg',
                    name: 'Shadow Spark Pants',
                    price: '600',
                },
                {
                    id: 4,
                    image: 'https://i.pinimg.com/736x/dc/78/8d/dc788d1174597674085e100f779e87fe.jpg',
                    name: 'Vie Red Lipstick',
                    price: '230',
                },
                {
                    id: 5,
                    image: 'https://i.pinimg.com/736x/3b/e4/f9/3be4f9792445891766ca15a691074d69.jpg',
                    name: 'Billini Crossbag',
                    price: '780',
                },
                {
                    id: 6,
                    image: 'https://i.pinimg.com/736x/0c/c8/64/0cc864f91b60a876ca83dff81b5efd14.jpg',
                    name: 'Adidas Samba',
                    price: '2,240',
                },
                {
                    id: 7,
                    image: 'https://i.pinimg.com/1200x/db/d3/94/dbd394b0edc22ca8a6b7df2a11cb47f0.jpg',
                    name: 'Aqua Flask',
                    price: '300'
                },
                {
                    id: 8,
                    image: 'https://i.pinimg.com/1200x/f9/28/3a/f9283ae23322f92966db481747a1b4f3.jpg',
                    name: 'Leopard Scarf',
                    price: '240'
                },
                {
                    id: 9,
                    image: 'https://i.pinimg.com/1200x/73/57/ca/7357ca5ff528e57584e6776900377781.jpg',
                    name: 'Minimalist Necklace',
                    price: '198'
                },
                {
                    id: 10,
                    image: 'https://i.pinimg.com/736x/72/53/d9/7253d908bb55c4337bc407ffb4dbd4bc.jpg',
                    name: 'Airpods Pro',
                    price: '3,560'
                },
                {
                    id: 11,
                    image: 'https://i.pinimg.com/736x/1d/19/b0/1d19b0a717c519c9a6cad03e3fd97152.jpg',
                    name: 'Iphone 17 Pro Max',
                    price: '71,999'
                },
                {
                    id: 12,
                    image: 'https://i.pinimg.com/736x/4d/ef/de/4defde357f3ddd45346d77497271f3c3.jpg',
                    name: 'MacBook Pro 16',
                    price: '92,999'
                },
                {
                    id: 13,
                    image: 'https://i.pinimg.com/1200x/7e/c7/5e/7ec75e0b57847e948e21c555ad3760c0.jpg',
                    name: 'Bather Tote Bag',
                    price: '249'
                },
                {
                    id: 14,
                    image: 'https://i.pinimg.com/736x/71/74/f3/7174f35ad5e171638d5e3334add0a537.jpg',
                    name: 'Libasol Polo Shirt',
                    price: '780'
                },
                {
                    id: 15,
                    image: 'https://i.pinimg.com/736x/fd/f4/ac/fdf4ac0295a27f230b753006469864f1.jpg',
                    name: 'YSL Perfume',
                    price: '5,700'
                },
                {
                    id: 16,
                    image: 'https://i.pinimg.com/736x/e1/b8/b8/e1b8b82704fa339629a4fbacbcd512b2.jpg',
                    name: 'Keychain',
                    price: '109'
                },
                {
                    id: 17,
                    image: 'https://i.pinimg.com/736x/2e/6e/a3/2e6ea3276c150775ce337e5df8dfef39.jpg',
                    name: 'Capybara Stuff',
                    price: '260'
                },
                {
                    id: 18,
                    image: 'https://i.pinimg.com/1200x/f5/6e/4b/f56e4ba9832e60a4988478bd61fc8010.jpg',
                    name: 'Light Blue Dress',
                    price: '$20'
                },
            ],
            choices: [
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-81ztm-mhkdwf4knta9c1@resize_w90_nl.webp',
                    name: 'Fullfilled by shopee'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-7ra0p-mb4xvtcan4um7d@resize_w90_nl.webp',
                    name: 'Flash Deals'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-7rase-m2rvxe6tt81eff@resize_w90_nl.webp',
                    name: 'Free shipping & Vouchers'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-81ztm-mh8mrk6pu5fse6@resize_w90_nl.webp',
                    name: 'Millions of Fashion Deals'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-50009109-d035ecb829748ba2404c468aa9ead53f@resize_w90_nl.webp',
                    name: 'Shopee Beauty'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-7ra0j-mbqceozizhxzc7@resize_w90_nl.webp',
                    name: 'Shopee Choice Daily $49'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-7ra0q-mcbzfrkklbf5ca@resize_w90_nl.webp',
                    name: 'Shopee Loyalty Silver'
                },
                {
                    id: 1,
                    image: 'https://down-ph.img.susercontent.com/file/ph-11134258-7ra0q-mcbzfrkklbf5ca@resize_w90_nl.webp',
                    name: 'Partner Promos'
                },
            ],
            categories: [
                {
                    image: 'https://down-ph.img.susercontent.com/file/2e9bfe13ce9cecfbfad8010b843651f6@resize_w640_nl.webp',
                    name: 'Mens Apparel'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/b3ae45e4ea16d61f0f6cf98ed623bb67@resize_w640_nl.webp',
                    name: 'obiles and Gadgets'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/34e01853a846ee2280853aa6792effca@resize_w640_nl.webp',
                    name: 'Mobiles Accesories'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/f88a53eadc71460a50ba49316235a5a5@resize_w640_nl.webp',
                    name: 'Home Entertainment'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/fbf1d6707dac5f09db46e60b87aae351@resize_w640_nl.webp',
                    name: 'Babies and Kids'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/e96e55c299602c20d369183378887a86@resize_w640_nl.webp',
                    name: 'Home And Living'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/f2423bdc8e19310ece9cf70c81e58897@resize_w640_nl.webp',
                    name: 'Groceries'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/aff648bd1cc6d00de3d908457de3e128@resize_w640_nl.webp',
                    name: 'Toys and Games'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/55267466ff3f0445bf28c21ddafd409c@resize_w640_nl.webp',
                    name: 'Womens Bag'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/9ab43516f83df1b1bc400edf56bccac7@resize_w640_nl.webp',
                    name: 'Womens Accessories'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/372cf1ccdb799772760d819408df35ba@resize_w640_nl.webp',
                    name: 'Womens Apparel'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/5906153a145fc19c2d808012f682f2fd@resize_w640_nl.webp',
                    name: 'Personal Care'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/15bcf95dddc19a5fb0fb0f9e777761a2@resize_w640_nl.webp',
                    name: 'Makeup'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/d31d29d2f160baeb7592964cd9090a52@resize_w640_nl.webp',
                    name: 'Home Appliances'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/25936be031f917470cb8c8ad9f311413@resize_w640_nl.webp',
                    name: 'Laptops and Computers'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/5a9d9bb1c39229501a6acec4f89fdc5c@resize_w640_nl.webp',
                    name: 'Camers'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/f12cfed5944ad868e181c6583a5a4426@resize_w640_nl.webp',
                    name: 'Sports'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/a3db43790bd5a473e606076fa4bc6717@resize_w640_nl.webp',
                    name: 'Mens Bag'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/4485e4fb0ed0372934c6e11ec3601d7c@resize_w640_nl.webp',
                    name: 'Mens Shoes'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/34e01853a846ee2280853aa6792effca@resize_w640_nl.webp',
                    name: 'Motor'
                },
            ],
            tops: [
                {
                    image: 'https://down-ph.img.susercontent.com/file/f2bcc5c6614dc974ddef90f64a26443c',
                    name: 'Fashionable'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/9e228630a161de8b374f7980b1fb43a9',
                    name: 'Tank Tops'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/9e228630a161de8b374f7980b1fb43a9',
                    name: 'Plus size Tops'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/aad0c67b84da53ebaff34fd78e27cc38',
                    name: 'Blouse'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/640fc9c4bbd4ba9103cc6ec1be82dd0c',
                    name: 'Diapers'
                },
                {
                    image: 'https://down-ph.img.susercontent.com/file/640fc9c4bbd4ba9103cc6ec1be82dd0c',
                    name: 'Maxi Dress'
                }
            ],

            showModal: false,
            showCart: false,
            history: false,
            searchbar: '',
        }
    },
    computed: {
        filteredProducts() {
            if (!this.forSearch.trim()) {
                return this.products
            }
            const query = this.forSearch.toLowerCase().trim();
            return this.products.filter(product =>
                product.name.toLowerCase().includes(query)
            )
        }
    },

    methods: {
        handleBuy() {
        },
        Modalbtn(index) {
            this.currentIndex = index;
            this.showModal = true;
        },
        close() {
            this.showModal = false;
        },
        closeProductModal() {
            this.$emit('closeaddModal')
        },
        add(newProduct) {
            this.products.push({ ...newProduct })
        },
        sendtoCart(product) {
            this.$emit('addtocart', { ...product });
            this.showModal = false
        },
        sendtohistory(){
            this.$emit('purchase', {...product})
        }
    },
}
</script>
<template>
    <div class="bg-amber-800/30 pt-3">
        <div class="flex justify-center">
            <div class="w-300 h-60 mt-30">
                <div class="flex">
                    <div class="w-200 h-55">
                        <div class="flex items-center gap-10">
                            <!-- <img class="w-45 mt-5 mx-3" src="../assets/images/relo.png" alt="">
                            <div class="mt-10">
                                <h1 class="text-2xl text-white mt-5">UP TO <span class="text-4xl font-black">30%
                                        OFF</span></h1>
                                <p class="text-white/90 text-sm">PER DTI B-PERMIT. Payment Methods are available, you
                                    can pay online or COD</p>
                            </div> -->
                            <img class="w-250 h-56 mr-2 mt-2"
                                src="https://i.pinimg.com/1200x/d2/df/1e/d2df1ea12c596b86317e0b47f44ea27c.jpg" alt="">
                        </div>
                    </div>
                    <div class="flex flex-col py-2">
                        <div class="w-95 h-25">
                            <img class="h-27 w-95"
                                src="https://i.pinimg.com/736x/d8/ee/36/d8ee365065620e7b95a31e0fea459ddb.jpg" alt="">
                        </div>
                        <div class="w-95 h-25">
                            <img class="h-27 w-95 my-4"
                                src="https://i.pinimg.com/736x/2b/a5/b1/2ba5b18836072d106e4a831072a5264a.jpg" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="flex justify-center gap-7 p-2">
            <div class="flex bg-white shadow-xl/10 gap-8 py-2 px-1">
                <div v-for="choice in choices">
                    <div class="py-2">
                        <img class="w-13" :src="choice.image" alt="">
                        <p class="text-[14px]">{{ choice.name }}</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="mt-5 flex justify-center">
            <div class="w-300 h-auto bg-white shadowl/xl">
                <h1 class="xl text-gray-500 p-5">CATEGORIES</h1>
                <hr class="text-gray-400">
                <div class="flex ">
                    <div class="grid lg:grid-cols-10 gap-3 mg:grid-cols-5 sm:grid-cols-2">
                        <div v-for="category in categories" class="hover:scale-102 cursor-pointer hover:shadow-xl/20">
                            <div class="flex justify-center">
                                <img class="w-20" :src="category.image" alt="">
                            </div>
                            <h1 class="text-[14px] text-center p-2">{{ category.name }}</h1>
                        </div>

                    </div>
                </div>
            </div>
        </div>

        <div class="flex justify-center">

            <div class="w-300 bg-white h-auto m-5">
                <h1 class="p-3 text-black/70"> TOP PRODUCTS</h1>
                <hr>
                <div class="grid grid-cols-6">
                    <div v-for="top in tops" class="border border-gray-200 cursor-pointer">
                        <div class="p-2">
                            <img class="w-40 p-2" :src="top.image" alt="">
                            <h1 class="text-center text-lg font-semibold">{{ top.name }}</h1>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="w-full h-auto bg-amber-800/30">
        <div class="flex justify-center">
            <div class="w-300 bg-white h-auto border-b-5 border-amber-900/80">
                <h1 class="text-center py-5 text-xl text-amber-900/90 font-semibold">DAILY DISCOVER</h1>
            </div>
        </div>
        <div class="flex justify-center">
            <div class="grid lg:grid-cols-6 gap-2 p-2 sm:grid-cols-1">
                <div v-for="(product, index) in filteredProducts" :key="product.id" 5class="">
                    <div class="w-48 h-auto hover:scale-106 hover:shadow-xl/10 rounded-xl cursor-pointer bg-white">
                        <img class="w-48 h-55" :src="product.image" alt="">
                        <div class="p-2 pb-3">
                            <div>
                                <h1 class="text-[15] font-semibold">{{ product.name }}</h1>
                            </div>
                            <div class="flex justify-between">
                                <h3 class="text-sm font-semibold text-red-600/80">₱{{ product.price }}.00</h3>
                                <svg @click="Modalbtn(index)"
                                    class="w-8 h-8 p-1 text-white bg-amber-900/80 rounded-full" aria-hidden="true"
                                    xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none"
                                    viewBox="0 0 24 24">
                                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                        stroke-width="2" d="M5 4h1.5L9 16m0 0h8m-8 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4Zm8 0a2 2 0 1 0 0 4 2 2 0 0
                                0 0-4Zm-8.5-3h9.25L19 7h-1M8 7h-.688M13 5v4m-2-2h4" />
                                </svg>
                            </div>

                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <Modal v-if="showModal" :selectedProduct="products[currentIndex]" @CancelModal="close" @addtocart="sendtoCart" />
    <Add v-if="addingProduct" @closeModal="closeProductModal" @submitProduct="add" />
</template>