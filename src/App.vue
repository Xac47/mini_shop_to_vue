<script setup>
import { onMounted, watch, ref, reactive } from 'vue'
import axios from 'axios'

import Header from './components/Header.vue'
import BlockInfo from './components/BlockInfo.vue'
import ProductList from './components/ProductList.vue'
// import Drawer from './components/Drawer.vue'

const products = ref([]) // { value: [] }

const filter = reactive({
  sortBy: '',
  searchQuery: ''
})

const fetchProducts = async () => {
  try {
    const params = {
      sortBy: filter.sortBy,
      searchQuery: filter.searchQuery
    }

    const { data } = await axios.get(
      `https://e7b3e3a30dc0a1a6.mokky.dev/products?title=*${filter.searchQuery}*&sortBy=${filter.sortBy}`
    )
    products.value = data
  } catch (error) {
    console.log(error)
  }
}

// Изменняет переменную sortBy
const onChangeSelect = (event) => {
  filter.sortBy = event.target.value
}

const onChangeSearchQuery = (event) => {
  filter.searchQuery = event.target.value
}

onMounted(fetchProducts)
watch(filter, fetchProducts) // При изменении указанной переменной (sortBy) вызывается функция fetchProducts
</script>

<template>
  <!-- <Drawer /> -->
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14 p-14">
    <Header />
    <div class="line w-full rounded-xl bg-gray-300 h-0.5 my-10"></div>
    <BlockInfo />
    <div class="block-main mt-10">
      <div class="block-main-start flex justify-between items-center">
        <h1 class="font-bold text-3xl">Все кроссовоки</h1>

        <div class="flex gap-5 items-center">
          <select
            @change="onChangeSelect"
            name=""
            id=""
            class="appearance-none cursor-pointer border border-gray-300 rounded-2xl py-3 px-6 pr-8 leading-tight focus:outline-none focus:border-blue-500 focus:ring-1 focus:ring-blue-500"
          >
            <option value="title">По названию</option>
            <option value="-price">Дороже</option>
            <option value="price">Дешевлее</option>
          </select>
          <form
            class="search-block flex gap-5 items-center p-3 rounded-2xl border border-gray-300 cursor-pointer"
          >
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
            <input @input="onChangeSearchQuery" class="outline-none" type="text" placeholder="Поиск..." value="" />
          </form>
        </div>
      </div>
      <ProductList :productList="products" />
    </div>
  </div>
</template>

<style scoped></style>
