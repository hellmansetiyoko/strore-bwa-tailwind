<script setup>
import GuestLayout from "@/Layouts/GuestLayout.vue";
import {Tools,Baby,Funiture,Gadget,MakeUp,Sneaker } from "@/assets/svg";
import { Banner } from "@/assets/img";
import { CategoriesCard, SectionHeader, TrendCategoriesCard } from "@/components";

const TrendsCategories= [
  { icon : Tools, category : 'Tools'},
  { icon : Baby, category : 'Baby'},
  { icon : Funiture, category : 'Funiture'},
  { icon : Gadget, category : 'Gadget'},
  { icon : Sneaker, category : 'Sneaker'},
  { icon : MakeUp, category : 'Make Up'},
];
</script>
<template>
  <GuestLayout>
    <header class="my-6 mt-12">
      <div
        class="relative"
      >
      <img :src="Banner" alt="" class="object-cover w-full rounded-md">
        <div class="absolute h-full top-32 left-8">
          <h2 class="text-amber-600 font-bold text-5xl w-1/2">
            Discount 50% Off All Members
          </h2>
          <h4 class="text-amber-700 font-light">
            Included tax pricing for U.S citizen or other countries
          </h4>
        </div>
      </div>
    </header>

    <div class="mt-12  space-y-10">
      <section>
        <section-header caption="Trends Categories" />
        <div class="mt-4">
          <div class="grid grid-cols-6 gap-20">
            <categories-card :category="value.category" v-for="(value, index) in TrendsCategories" :key="index">
              <template #icon>
                <img :src="value.icon" alt="" />
              </template>
            </categories-card>
          </div>
        </div>
      </section>
      <section>
        <section-header :caption="`Trends Categories`" />
        <div class="mt-4">
          <div class="grid grid-cols-4 gap-4">
            <div v-for="index in 8" :key="index">
              <TrendCategoriesCard category="category" price="$2020">
                <template #banner>
                  <img :src="Banner" alt="" class="rounded-md h-32" />
                </template>
                </TrendCategoriesCard>
            </div>
          </div>
        </div>
      </section>
    </div>
 
  </GuestLayout>
</template>
