<template>
  <header class="flex justify-between">
    <div class="header-start flex gap-4">
      <img src="/logo.png" alt="" />
      <div class="header-title flex flex-col justify-center gap-2">
        <h1 class="text-xl font-bold uppercase">VUE SHOP</h1>
        <p class="text-slate-500">Магазин лучших кроссовок</p>
      </div>
    </div>
    <div class="header-end flex gap-10 items-center">
      <div class="cart flex gap-2 text-gray-500 cursor-pointer hover:text-black transition duration-300">
        <img src="/cart.svg" alt="" />
        <span>1205 руб.</span>
      </div>
      <div class="favorites flex gap-2 text-gray-500 cursor-pointer hover:text-black transition duration-300">
        <img src="/heart.svg" alt="" />
        <span>Закладки</span>
      </div>
      <div class="profile flex gap-2 text-gray-500 cursor-pointer hover:text-black transition duration-300">
        <img src="/profile.svg" alt="" />
        <span>Профиль</span>
      </div>
    </div>
  </header>
</template>
