<template>
    <div class="flex items-center max-w-md mx-auto gap-5">
        <!-- Left Arrow Button -->
        <button @click="prevCaseStudy"
            class="w-10 h-10 flex items-center justify-center bg-transparent border-2 border-gray-400 rounded-full hover:bg-gray-100 focus:outline-none">
            <svg class="w-4 h-4 text-gray-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
            </svg>
        </button>

        <!-- Pagination Dots -->
        <div class="flex space-x-2">
            <button v-for="(dot, index) in dots" :key="index" @click="handleDotClick(index)"
                :class="{ 'bg-black': index === activeIndex, 'bg-gray-400': index !== activeIndex }"
                class="w-3 h-3 rounded-full focus:outline-none"></button>
        </div>

        <!-- Right Arrow Button  -->
        <button @click="nextCaseStudy"
            class="w-10 h-10 flex items-center justify-center bg-transparent border-2 border-gray-400 rounded-full hover:bg-gray-100 focus:outline-none">
            <svg class="w-4 h-4 text-gray-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
            </svg>
        </button>
    </div>
</template>

<script setup lang="ts">
import { ref, defineEmits } from 'vue';

const dots = ref([1, 2, 3, 4, 5, 6, 7, 8, 9]);
const activeIndex = ref(0);
const emit = defineEmits(['prev', 'next', 'select']);

function prevCaseStudy() {
    emit('prev');
}

function nextCaseStudy() {
    emit('next');
}

function handleDotClick(index: number) {
    activeIndex.value = index;
    emit('select', index);
}
</script>

<style scoped></style>
