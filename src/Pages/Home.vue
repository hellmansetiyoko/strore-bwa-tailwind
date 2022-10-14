<script setup>
import { Banner } from "./assets/img";
import { ComputerDesktopIcon } from "@heroicons/vue/24/outline";
import BasicLink from "./components/BasicLink.vue";
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
        <nav class="flex justify-between">
          <div class="flex align-middle">
            <ComputerDesktopIcon class="h-8 w-8 text-slate-800" />
          </div>
          <div class="">
            <ul class="flex gap-8">
              <li v-for="(menu, index) in menu" :key="index">
                <BasicLink :url="menu.url" :text="menu.target" />
              </li>
            </ul>
          </div>
        </nav>

        <header class="mt-6 mb-6">
          <div
            class="rounded-md bg-cover bg-center col-span-1 h-96 px-8"
            :style="{
              'background-image': `url('${Banner}')`,
            }"
          >
            <div class="flex flex-col justify-center gap-2 h-full">
              <h2 class="text-amber-600 font-bold text-5xl w-1/3">
                Discount 50% Off All Members
              </h2>
              <h4 class="text-amber-700 w-1/5 font-light">
                Included tax pricing for U.S citizen or other countries
              </h4>
            </div>
          </div>
        </header>

        <section class="mt-8">
          <h3 class="font-Poppins font-medium text-lg text-[#0C0D36]">
            Trend Category
          </h3>

          <div class="mt-4">
            <div class="grid grid-cols-6 gap-20">
              <div
                v-for="index in 6"
                :key="index"
                class="
                  bg-gray-200
                  rounded-md
                  grid
                  place-content-center
                  pt-4
                  pb-4
                  flex-none
                "
              >
                <div
                  class="
                    bg-gray-300
                    rounded-full
                    grid
                    place-content-center
                    h-24
                    w-24
                    mx-auto
                  "
                >
                  <ComputerDesktopIcon class="h-12 w-12 text-gray-700" />
                </div>
                <p
                  class="
                    text-center
                    font-normal
                    text-[#0C0D36]
                    tracking-wider
                    pt-2
                  "
                >
                  Gadget
                </p>
              </div>
            </div>
          </div>
        </section>

        <section class="mt-8">
          <h3 class="font-Poppins font-medium text-lg text-[#0C0D36]">
            New Product
          </h3>

          <div class="mt-4">
            <div class="grid grid-cols-4 gap-4">
              <div v-for="index in 8" :key="index">
                <div class="space-y-2">
                  <figure>
                    <img :src="Banner" alt="" class="rounded-md h-32" />
                  </figure>
                  <figcaption class="font-medium text-xl text-[#0C0D36]">
                    Apple Watch
                  </figcaption>
                  <figcaption class="font-light text-orange-500">
                    Apple Watch
                  </figcaption>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap");
/* * {
  outline: 1px red solid;
} */
</style>
