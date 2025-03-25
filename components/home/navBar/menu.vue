
<template>
 <div class="container fixed">
<!-- Menu Button / Close Button -->
<button
@click="toggleMenu"
class="fixed top-2 right-8 z-50 flex items-center justify-center w-24 h-24 bg-pink-200  rounded-full shadow-lg transition duration-300 ease-in-out hover:bg-gray-700 hover:text-white"
>
<span v-if="!isOpen" class="font-normal text-xs ">Menu</span>
<span v-else class="font-medium">X</span>
</button>

<!-- Fullscreen Menu Overlay -->
<div
v-if="isOpen"

class="fixed inset-0 bg-[#EEFAFD] bg-opacity-85 flex items-start pl-20 pt-28 z-40 transition-opacity duration-300 ease-in-out"
>
<ul class="text-gray-700 text-5xl space-y-14">
  <ul class="text-gray-700 text-5xl space-y-14">
  <li><a href="#home" v-scroll-to="'#home'">Home</a></li>
  <li><a href="#how-it-works" v-scroll-to="'#how-it-works'">How We Work</a></li>
  <li><a href="#our-team" v-scroll-to="'#our-team'">Our Team</a></li>
  <li><a href="#contact-us" v-scroll-to="'#contact-us'">Contact Us</a></li>
</ul>
</ul>
</div>
</div>
</template>

<script setup>
import { ref } from 'vue';
 
const isOpen = ref(false);

function toggleMenu() {
  isOpen.value = !isOpen.value;
}
</script>
<style>

</style>