<template>
  <div class="grid grid-cols-4 gap-[24px]">

    <div
        v-for="product in products"
        :key="product.id"
        class="flex flex-col rounded-[4px] bg-white gap-[8px]"
    >
      <div class="relative bg-[#F8F8FA] pt-[100%]">
        <svg class="absolute top-[70px] left-[77px]" width="60" height="60" viewBox="0 0 60 60" fill="none" xmlns="http://www.w3.org/2000/svg">
          <g opacity="0.5" clip-path="url(#clip0_11521_786)">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M58.23 11.1487C58.7521 11.3571 59.1997 11.7171 59.5152 12.1823C59.8307 12.6476 59.9996 13.1966 60 13.7587V46.2412C59.9996 46.8034 59.8307 47.3524 59.5152 47.8177C59.1997 48.2829 58.7521 48.6429 58.23 48.8512L31.0425 59.7262C30.3721 59.9944 29.6242 59.9944 28.9538 59.7262L1.76625 48.8512C1.24488 48.6423 0.79802 48.282 0.483227 47.8169C0.168434 47.3517 0.000130725 46.8029 0 46.2412L0 13.7587C0.000130725 13.1971 0.168434 12.6483 0.483227 12.1831C0.79802 11.718 1.24488 11.3577 1.76625 11.1487L27.9113 0.689995L27.9488 0.678745L28.9538 0.273745C29.6253 0.00461759 30.3747 0.00461759 31.0463 0.273745L32.055 0.678745L32.0925 0.689995L58.23 11.1487ZM39.015 7.5L15.9375 16.7287L6.9225 13.125L3.75 14.3962V15.8962L28.125 25.6462V55.3537L30 56.1037L31.875 55.3537V25.65L56.25 15.9V14.4L53.0775 13.1287L30 22.3537L20.985 18.75L44.0625 9.52125L39.015 7.5Z" fill="#A6A9C7"/>
          </g>
          <defs>
            <clipPath id="clip0_11521_786">
              <rect width="60" height="60" fill="white"/>
            </clipPath>
          </defs>
        </svg>

      </div>

      <div class="flex flex-grow flex-col gap-[16px]">
        <span class="text-[#AAAAAA] text-[14px]">Бренд</span>

        <h3 class="text-[#333333] break-words text-[14px]/[16px]">
          {{ product.name }}
        </h3>

        <div class="flex gap-[8px]">
          <span class="text-[16px]/[14px] font-bold text-[#333333]">{{ product.price }} ₽</span>
          <span v-if="product.oldPrice && product.isAvailable" class="text-[12px] text-[#AAAAAA] line-through">{{ product.oldPrice }} ₽</span>
        </div>

        <div class="mt-auto">
          <button v-if="product.isAvailable" class="rounded-[4px] bg-[#FFFFFF] border py-[16px] px-[12px] text-center text-[14px] font-semibold text-[#7397F5] hover:bg-blue-600">
            Купить
          </button>
          <button v-else class="w-full rounded-[4px] border border-[#AAAAAA] py-[12px] px-[16px] text-center text-[14px] font-semibold text-[#AAAAAA] hover:bg-gray-50">
            Сообщить о поступлении
          </button>
        </div>
      </div>
    </div>

  </div>
</template>

<script setup>
import { ref } from 'vue';

const products = ref([
  { id: 1, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: false },
  { id: 2, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 3, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 4, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 5, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 6, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 7, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 8, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 9, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
  { id: 10, name: 'Полное название товара в несколько строк для вида с обрывом в конце...', price: '5 990', oldPrice: '7 990', isHit: true, isAvailable: true },
]);

</script>
