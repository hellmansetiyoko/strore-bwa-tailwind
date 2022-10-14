<script setup>
import { Banner } from "@/assets/img";
const Props = defineProps([
    'category',
    'price'
])
</script>
<template>
  <div>
    <figure class="mb-4">
        <slot name="banner"/>
    </figure>
    <figcaption class="text-xl text-[#0C0D36]">
      {{ category }}
    </figcaption>
    <figcaption class="font-light text-orange-500">{{ price }}</figcaption>
  </div>
</template>