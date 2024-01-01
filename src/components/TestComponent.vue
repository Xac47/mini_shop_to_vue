<script setup>
defineProps({
    'title': String,
    'price': Number,
    'isAdded': Boolean,
})
</script>

<template>

    <div class="block-main">
        <div class="product-item p-2">
            <h2>Товар: {{ title }}</h2>
            <h3>Цена: {{ price }}руб</h3>
            <h4>Добавлено: {{ isAdded }}</h4>
        </div>
    </div>

</template>


<style scoped>

</style>