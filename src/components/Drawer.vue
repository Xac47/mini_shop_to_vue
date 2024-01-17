<script setup>
import DrawerHead from './DrawerHead.vue'
import DrawerEnd from './DrawerEnd.vue';
import CartItemList from './CartItemList.vue'
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full bg-black z-10 opacity-50"></div>
  <div class="bg-white w-1/4 h-full fixed top-0 right-0 z-20 p-10 flex flex-col justify-between">
    <div>
      <DrawerHead />
      <CartItemList />
    </div>

    <DrawerEnd />

  </div>
</template>
