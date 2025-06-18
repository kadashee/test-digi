<template>
  <div class="w-[280px] bg-white flex flex-col gap-[8px]">

    <div class="flex items-center justify-between">
      <h3 class="text-[16px] font-semibold text-[#333333]">Бренд</h3>
      <button class="text-[12px] text-[#AAAAAA] underline">
        Очистить
      </button>
    </div>

    <div class="relative border border-[#D5D5D5] rounded-[4px] text-[14px]">
      <span class="pointer-events-none absolute inset-y-0 left-5 flex items-center">
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<g opacity="0.3">
<path fill-rule="evenodd" clip-rule="evenodd" d="M7.33333 2.75C4.80203 2.75 2.75 4.80203 2.75 7.33333C2.75 9.86464 4.80203 11.9167 7.33333 11.9167C9.86464 11.9167 11.9167 9.86464 11.9167 7.33333C11.9167 4.80203 9.86464 2.75 7.33333 2.75ZM1.25 7.33333C1.25 3.9736 3.9736 1.25 7.33333 1.25C10.6931 1.25 13.4167 3.9736 13.4167 7.33333C13.4167 10.6931 10.6931 13.4167 7.33333 13.4167C3.9736 13.4167 1.25 10.6931 1.25 7.33333Z" fill="#333333"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M10.5698 10.5696C10.8627 10.2768 11.3375 10.2768 11.6304 10.5696L14.5304 13.4696C14.8233 13.7625 14.8233 14.2374 14.5304 14.5303C14.2375 14.8232 13.7627 14.8232 13.4698 14.5303L10.5698 11.6303C10.2769 11.3374 10.2769 10.8625 10.5698 10.5696Z" fill="#333333"/>
</g>
</svg>

      </span>
      <input type="text" placeholder="Поиск" class="block w-full pl-12 py-[10px] rounded-[4px] border-[#D5D5D5] text-[14px] focus:border-blue-500 focus:ring-blue-500" />
    </div>

    <div class="max-h-[180px] overflow-y-auto pr-[16px]">
      <label v-for="n in 15" :key="n" class="flex cursor-pointer items-center justify-between rounded-md p-2 hover:bg-gray-100">
        <div class="flex items-center gap-[12px]">
          <input
              type="checkbox"
              :checked="n === 1"
              class="h-5 w-5 focus:ring-blue-500"
          />
          <span class="text-[14px] text-[#333333]">Атрибут</span>
        </div>
        <span class="text-[12px] text-[#AAAAAA]">3</span>
      </label>
    </div>

  </div>
</template>

<script setup>

</script>
