<template>
  <div class="w-[280px] flex flex-col justify-between gap-[16px]">
<div>
    <h3 class="text-center">Цена</h3>
</div>

    <div class="flex items-center gap-2">

      <div class="relative w-1/2">
        <input
            v-model="priceFrom"
            type="number"
            class="w-full h-[36px] text-[#333333] rounded-[4px] border border-[#D5D5D5] pl-8 pr-[8px] py-[10px] text-[14px] focus:border-black focus:outline-none placeholder:text-black"
            placeholder="5 500"
        />
        <span class="absolute left-3 top-1/2 -translate-y-1/2 text-[12px] text-[#AAAAAA]">от</span>
      </div>

      <div class="text-gray-400">—</div>

      <div class="relative w-1/2">
        <input
            v-model="priceTo"
            type="number"
            class="w-full h-[36px] text-[#333333] rounded-[4px] border border-[#D5D5D5] pl-8 pr-[8px] py-[10px] text-[14px] focus:border-black focus:outline-none placeholder:text-black"
            placeholder="5 500"
        />
        <span class="absolute left-3 top-1/2 -translate-y-1/2 text-[12px] text-[#AAAAAA]">до</span>
      </div>

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Создаем реактивные переменные для хранения значений "от" и "до"
const priceFrom = ref('');
const priceTo = ref('');
</script>
