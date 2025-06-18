<template>
  <Header />

  <div class="mx-auto max-w-7xl px-8 mt-8">
    <div class="flex gap-8">

      <aside class="w-[288px] shrink-0">
        <category-filter />
        <slider-filter class="mt-6" />
        <checkbox-brand class="mt-6" />
        <checkbox-size class="mt-6" />
      </aside>
      <main class="flex-1">
        <products />
      </main>

    </div>
  </div>
</template>
