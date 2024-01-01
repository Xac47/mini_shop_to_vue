<template>
  <div class="block-info rounded-2xl flex justify-between relative">
    <div class="block-info-start">
      <img src="/image_7.png" alt="" class="p-4" />
      <div class="block-info-title p">
        <h1 class="text-6xl text-lime-500 font-bold pl-14 pt-4">Stan Smith,</h1>
        <h1 class="text-6xl text-black font-bold pl-14">Forever!</h1>
      </div>
      <div class="block-info-button pl-14 pt-4">
        <button
          class="block-info-button rounded-3xl bg-lime-500 text-white font-bold pt-2 pb-2 pl-14 pr-14"
        >
          Купить
        </button>
      </div>
    </div>
    <div class="block-info-end">
      <img src="/image_6.png" alt="" />
    </div>
    <div class="block-arrow absolute -right-6 top-1/2 -translate-y-1/2">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="51"
        height="51"
        viewBox="0 0 51 51"
        fill="none"
      >
        <g filter="url(#filter0_d_60_240)">
          <rect
            x="43"
            y="39"
            width="35"
            height="35"
            rx="17.5"
            transform="rotate(-180 43 39)"
            fill="white"
          />
        </g>
        <path
          d="M24 17L29 22L24 27"
          stroke="#C8C8C8"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <defs>
          <filter
            id="filter0_d_60_240"
            x="0"
            y="0"
            width="51"
            height="51"
            filterUnits="userSpaceOnUse"
            color-interpolation-filters="sRGB"
          >
            <feFlood flood-opacity="0" result="BackgroundImageFix" />
            <feColorMatrix
              in="SourceAlpha"
              type="matrix"
              values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
              result="hardAlpha"
            />
            <feOffset dy="4" />
            <feGaussianBlur stdDeviation="4" />
            <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.04 0" />
            <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_60_240" />
            <feBlend
              mode="normal"
              in="SourceGraphic"
              in2="effect1_dropShadow_60_240"
              result="shape"
            />
          </filter>
        </defs>
      </svg>
    </div>
  </div>
</template>
