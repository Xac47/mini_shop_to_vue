<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isAdded: Boolean,
  isFavorite: Boolean
})
</script>

<template>
  <div
    class="block-item rounded-3xl border-2 border-gray-100 p-4 relative cursor-pointer hover:-translate-y-2 hover:shadow-xl transition duration-300">
    <img
      :src="!isFavorite ? '/like-1.svg' : '/like-2.svg'"
      alt="like"
      class="w-10 h-10 absolute top-12 left-4"
    />
    <img :src="imageUrl" alt="product" class="w-120 h-120" />
    <p class="mt-2">{{ title }}</p>

    <div class="block-item-wrapper flex justify-between mt-4">
      <div class="block-item-wrapper-info flex flex-col">
        <span class="text-slate-500">Цена:</span>
        <b>{{ price }} руб</b>
      </div>
      <img :src="!isAdded ? '/plus.svg' : '/checked.svg'" alt="plus" />
    </div>
  </div>
</template>
