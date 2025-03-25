<!-- <template>
  <div class="flex justify-between items-center h-[4vw]">
    <div class="h-[6.4vw] bg-[#AEDDFF] p-3 rounded-se-3xl rounded-es-3xl">
      <img
        src="@/assets/logo.png"
        alt="apxzone logo"
        class="w-full h-full rounded-se-3xl rounded-es-3xl"
      />
    </div>

    <div
      class="mr-[10%] bg-[#AEDDFF] text-blue-700 py-4 px-6 rounded-lg font-extrabold rounded-se-xl rounded-es-xl"
    >
      {{ currentSection }}
    </div>

    <button
      @click="toggleMenu"
      class="fixed top-2 right-8 z-50 flex items-center justify-center w-24 h-24 bg-[#7dc0f1] rounded-full shadow-lg transition duration-300 ease-in-out hover:bg-[#b7d5e9] hover:text-black text-white"
    >
      <span v-if="!isOpen" class="font-bold text-sm ">Menu</span>
      <span v-else class="font-medium">X</span>
    </button>
  </div>

  <div
    v-if="isOpen"
    class="fixed inset-0 bg-[#EEFAFD] bg-opacity-85 flex items-start pl-20 pt-28 z-40 transition-opacity duration-300 ease-in-out"
  >
    <ul class="text-gray-700 text-5xl space-y-14">
      <li><a href="#home" v-scroll-to="'#home'">Home</a></li>
      <li>
        <a href="#how-it-works" v-scroll-to="'#how-it-works'">How We Work</a>
      </li>
      <li><a href="#our-team" v-scroll-to="'#our-team'">Our Team</a></li>
      <li><a href="#contact-us" v-scroll-to="'#contact-us'">Contact Us</a></li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);

function toggleMenu() {
  isOpen.value = !isOpen.value;
}
const props = defineProps({
  currentSection: {
    type: String,
    required: true,
  },
});
</script>

<style></style> -->
<template>
  <div class="flex justify-between items-center h-[4vw]">
    <div class="h-[6.4vw] bg-[#AEDDFF] p-3 rounded-se-3xl rounded-es-3xl">
      <img
        src="@/assets/logo.png"
        alt="apxzone logo"
        class="w-full h-full rounded-se-3xl rounded-es-3xl"
      />
    </div>

    <div
      class="ml-[60%] bg-[#AEDDFF] text-blue-700 py-4 px-6 rounded-lg font-comfortaabold rounded-se-xl rounded-es-xl"
    >
      {{ currentSection }}
    </div>

    <button
      @click="toggleMenu"
      class="fixed top-2 right-8 z-50 flex items-center justify-center w-24 h-24 bg-[#7dc0f1] rounded-full shadow-lg transition duration-300 ease-in-out text-white btn"
    >
      <span v-if="!isOpen" class="font-comfortaabold text-sm label">Menu</span>
      <span v-else class="font-comfortaabold label">X</span>
      <div class="bg"></div>
    </button>
  </div>

  <!-- Menu container with transition -->
  <div
    v-show="isOpen"
    ref="menuContainer"
    class="fixed inset-0  bg-opacity-95 flex items-start pl-20 pt-28 z-40"
  >
    <ul class="text-white text-5xl space-y-14" v-if="isMenuItemsVisible">
      <li v-for="(item, index) in menuItems" :key="index">
        <a :href="item.href" v-scroll-to="item.href">{{ item.label }}</a>
      </li>
    </ul>
  </div>
  <div class="bg-expand rounded-full"></div>
</template>

<script setup>
import { ref } from "vue";
import gsap from "gsap";

const isOpen = ref(false);
const isMenuItemsVisible = ref(false);

function toggleMenu() {
  if (!isOpen.value) {
    isOpen.value = true;
    gsap.fromTo(
      ".bg-expand",
      { scale: 0, opacity: 1 },
      {
        scale: 2.6, // Ensure this is large enough to cover the screen
        duration: 1,
        ease: "power2.inOut",
        onComplete: () => {
          isMenuItemsVisible.value = true;
        },
      }
    );
  } else {
    gsap.to(".bg-expand", {
      scale: 0,
      duration: 1,
      ease: "power2.inOut",
      onComplete: () => {
        isOpen.value = false;
        isMenuItemsVisible.value = false;
      },
    });
  }
}

const menuItems = [
  { label: "Home", href: "" },
  { label: "How We Work", href: "#how-it-works" },
  { label: "Our Team", href: "#our-team" },
  { label: "Contact Us", href: "#contact-us" },
];
const props = defineProps({
  currentSection: {
    type: String,
    required: true,
  },
});
</script>

<style>
.btn {
  position: relative;
  overflow: hidden;
  cursor: pointer;
}

.label {
  position: relative;
  z-index: 1;
  transition: color 0.3s ease-out;
}



.bg-expand {
  position: fixed;
  top: 10%;
  left: 90%;
  width: 100%;
  height: 100%;
  background-color: #7DC0F1;
  transform: translate(-50%, -50%) scale(0);
  z-index: 39; /* Below menu items */
  pointer-events: none;
}
</style>
