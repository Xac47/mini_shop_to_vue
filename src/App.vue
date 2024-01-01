<script setup>
import Header from './components/Header.vue'
import BlockInfo from './components/BlockInfo.vue'
import Product from './components/Product.vue'
</script>

<template>
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14 p-14">
    <Header />
    <div class="line w-full rounded-xl bg-gray-300 h-0.5 my-10"></div>
    <BlockInfo />
    <div class="block-main mt-10">
      <div class="block-main-start flex justify-between items-center">
        <h1 class="font-bold text-3xl">Все кроссовоки</h1>
        <form class="search-block flex gap-5 items-center p-4 rounded-2xl border-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            viewBox="0 0 16 16"
            fill="none"
          >
            <path
              d="M15.25 15.25L11.8855 11.8795L15.25 15.25ZM13.75 7.375C13.75 9.06576 13.0784 10.6873 11.8828 11.8828C10.6873 13.0784 9.06576 13.75 7.375 13.75C5.68424 13.75 4.06274 13.0784 2.86719 11.8828C1.67165 10.6873 1 9.06576 1 7.375C1 5.68424 1.67165 4.06274 2.86719 2.86719C4.06274 1.67165 5.68424 1 7.375 1C9.06576 1 10.6873 1.67165 11.8828 2.86719C13.0784 4.06274 13.75 5.68424 13.75 7.375V7.375Z"
              stroke="#E4E4E4"
              stroke-width="2"
              stroke-linecap="round"
            />
          </svg>
          <input type="text" placeholder="Поиск..." />
        </form>
      </div>
      <div class="block-main-end mt-10 grid grid-cols-4 flex gap-10">
        <Product />
        <Product />
        <Product />
        <Product />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
