<script setup>
defineProps({
  title: String,
  price: Number,
  imageUrl: String
})
</script>


<template>
  <div class="border border-slate-200 rounded-3xl p-4 mt-5 flex items-center gap-5 cursor-pointer hover:-translate-y-2 hover:shadow-xl transition duration-300">
    <img :src="imageUrl" alt="photo" class="w-20 h-22" />

    <div class="flex flex-col gap-2">
      <p>{{ title }}</p>

      <div class="flex justify-between">
        <span class="font-bold">{{ price }} руб</span>
        <img src="/close.svg" alt="plus" class="cursor-pointer opacity-50 hover:opacity-100 transition duration-300" />
      </div>
    </div>
  </div>
</template>
