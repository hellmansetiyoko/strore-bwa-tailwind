<template>
  <a
    :href="url"
    class="text-sm font-Poppins text-violet-900 font-normal"
    v-text="Text"
  >
  </a>
</template>

<script setup>
import { defineProps } from "vue";
const prop = defineProps({
  url: String,
  Text: String,
});
</script>