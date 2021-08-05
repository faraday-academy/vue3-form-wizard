<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/cart">Cart</router-link> |
    <router-link to="/checkout">Checkout</router-link>
  </div>
  <div class="p-grid">
    <div class="p-col-4 p-offset-4">
      <router-view />
    </div>
  </div>
</template>
