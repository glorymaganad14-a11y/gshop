<script>
import Nav from './components/Nav.vue'
import Home from './components/Home.vue'
import Cart from './components/Cart.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Nav,
    Home,
    Cart, 
    Footer
  },

  data() {
    return {
      showAddModal: false,
      currentPage: 'home',
      cartItems: []
    }
  },
  methods: {
    addModal() {
      this.showAddModal = true;
    },
    changePage(page) {
      this.currentPage = page;
    },

    addToCart(product) {
      this.cartItems.push({...product});
    }
  }
}
</script>

<template>
  <Nav 
  @OpenAddModal="showAddModal = true" 
  @goTo="changePage" />

  <Home 
  v-if="currentPage === 'home'" 
  :addingProduct="showAddModal" 
  @closeaddModal="showAddModal = false"
  @addtocart="addToCart" />

  <Cart 
  v-if="currentPage === 'showCart'" 
  :cartitems="cartItems" />
  <Footer />
</template>