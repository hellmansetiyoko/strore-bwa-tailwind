<script setup>
const Props = defineProps(["category"]);
</script>
<template>
  <div
    class="bg-gray-200 rounded-md grid place-content-center pt-8 pb-8 shadow-md"
  >
    <div class="bg-gray-300 rounded-full grid place-content-center h-24 w-24">
      <div class="h-10 w-10 flex text-gray-700">
        <slot name="icon" />
      </div>
    </div>
    <p class="text-center font-normal text-[#0C0D36] tracking-wider pt-2">
      {{ category }}
    </p>
  </div>
</template>
