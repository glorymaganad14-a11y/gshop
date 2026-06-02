<script>
import Nav from './components/Nav.vue'
import Home from './components/Home.vue'
import Cart from './components/Cart.vue'
import History from './components/History.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Nav,
    Home,
    Cart,
    History,
    Footer
  },
  data() {
    return {
      showAddModal: false,
      currentPage: 'home',
      cartItems: [],
      checkout: [],
      searchbar: ''
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
      this.cartItems.push({ ...product });
    },
    clickcheckOut(product) {
      this.checkout.push({ ...product })
    },
    handleSearch(search) {
      this.searchbar = search;
    }
  }
}
</script>

<template>
  <Nav @OpenAddModal="showAddModal = true" @goTo="changePage" @searchBar="handleSearch" />
  <Home v-if="currentPage === 'home'" :addingProduct="showAddModal" @closeaddModal="showAddModal = false"
    @addtocart="addToCart" :forSearch="searchbar" />

  <Cart v-if="currentPage === 'showCart'" :cartitems="cartItems" />
  <History v-if="currentPage === 'history'" @purchase="clickcheckOut" :purchased="checkout"/>
  <Footer />
</template>