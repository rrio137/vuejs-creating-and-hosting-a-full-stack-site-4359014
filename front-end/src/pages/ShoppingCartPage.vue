<template>
  <h1>Shopping Cart</h1>
  <div v-if="cartItems.length > 0">
    <ShoppingCartList :cartItems="cartItems"/>
    <button class="checkout-button">Proceed to checkout</button>
  </div>
  <div v-if="cartItems.length === 0">
    You have no items in your cart
  </div>
</template>

<script>
import { cartItems } from '../temp-data';
import ShoppingCartList from '@/components/ShoppingCartList.vue';

export default {
  name: "ShoppingCartPage",
  components: {
    ShoppingCartList,
  },
  data() {
    return {
      cartItems,
    }
  }
}
</script>