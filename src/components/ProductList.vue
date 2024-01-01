<script setup>
import Product from './Product.vue'
</script>

<template>
  <div class="block-main-end mt-10 grid grid-cols-4 flex gap-10">
    <Product imageUrl="/sneakers/sneakers-1.jpg" title="Кроссовки" price="2500" :isAdded="false" :isFavorite="true"/>
    <Product imageUrl="/sneakers/sneakers-2.jpg" title="Кроссовки" price="2500" :isAdded="false" :isFavorite="true"/>
    <Product imageUrl="/sneakers/sneakers-3.jpg" title="Кроссовки" price="2500" :isAdded="true" :isFavorite="false"/>
    <Product imageUrl="/sneakers/sneakers-4.jpg" title="Кроссовки" price="2500" :isAdded="false" :isFavorite="false"/>
    <Product imageUrl="/sneakers/sneakers-5.jpg" title="Кроссовки" price="2500" :isAdded="true" :isFavorite="true"/>
    <Product imageUrl="/sneakers/sneakers-6.jpg" title="Кроссовки" price="2500" :isAdded="false" :isFavorite="true"/>
    <Product imageUrl="/sneakers/sneakers-7.jpg" title="Кроссовки" price="2500" :isAdded="true" :isFavorite="true"/>
    <Product imageUrl="/sneakers/sneakers-8.jpg" title="Кроссовки" price="2500" :isAdded="true" :isFavorite="false"/>
  </div>
</template>
