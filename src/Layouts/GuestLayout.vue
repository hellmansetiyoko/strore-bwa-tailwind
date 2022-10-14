<script setup>
import BasicLink from "@/components/BasicLink.vue";
import { Logo } from "@/assets/svg";

const menu = [
  { target: "Home", url: "/" },
  { target: "Category", url: "#" },
  { target: "Reward", url: "#" },
  { target: "Sign Up", url: "#" },
];
</script>
<template>
  <div class="bg-white mb-8 font-Poppins">
    <div class="max-w-7xl mx-auto">
      <div class="pt-6">
        <nav class="flex justify-between align-middle">
          <div class="flex align-middle">
            <img :src="Logo" class="text-slate-800" />
          </div>
          <div>
            <ul class="flex gap-x-12 pt-4">
              <li v-for="(menu, index) in menu" :key="index">
                <BasicLink :url="menu.url" :text="menu.target" />
              </li>
            </ul>
          </div>
        </nav>
        <slot />
      </div>
    </div>
      <footer class="w-full grid place-items-center mt-60 text-gray-600">
    2019 Copyright Store. All Rights Reserved.
  </footer>
  </div>


</template>

<style>
/* * {
  outline: 1px red solid;
} */
</style>
