<template>
  <div>
    <div class="flex flex-col gap-4 mt-7 mb-5">
      <div class="flex gap-2">
        <span>Итого:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>12 900 руб</b>
      </div>

      <div class="flex gap-2">
        <span>Налог: 5%</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>1 450 руб</b>
      </div>
    </div>

    <button
      disabled=""
      class="bg-lime-500 text-white rounded-xl p-4 w-full transition duration-300 hover:bg-lime-600 active:bg-lime-700 disabled:bg-slate-300 cursor-pointer"
    >
      Оформить заказ
    </button>
  </div>
</template>
