<template>
  <div class="w-[280px] bg-white flex flex-col gap-[8px]">

    <h3 class="text-[16px] font-semibold text-[#333333] text-center">Размер</h3>

    
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
