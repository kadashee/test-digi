<template>
  <div class="w-[280px] bg-white">
    <a
        v-for="n in itemCount"
        :key="n"
        href="#"
        class="flex cursor-pointer items-center h-[30px]"
        :class="{
        'justify-center bg-[#E2EFFF]': activeItemIndex === n,
        'justify-between': activeItemIndex !== n
      }"
        @click.prevent="setActive(n)"
    >
      <span class="text-[14px] text-[#333333]">Название категории</span>

      <span
class="text-sm text-[#333333]"
            :class="{ 'hidden': activeItemIndex === n }"
            >
        3
      </span>
    </a>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const itemCount = 4;
const activeItemIndex = ref(null);
const setActive = (index) => {
  if (activeItemIndex.value === index) {
    activeItemIndex.value = null;
  } else {
    activeItemIndex.value = index;
  }
}
</script>
