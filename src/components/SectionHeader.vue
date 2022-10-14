<script setup>
const props = defineProps([
    'caption',
])
</script>
<template>
    <h3 class="font-medium text-2xl text-[#0C0D36]">
        {{ caption }}
    </h3>
</template>
