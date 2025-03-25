<template>
    <div class="container p-4">
      <div class="flex flex-col md:flex-row xl:space-y-6 space-y-0 lg:space-x-6 h-[100%] w-full">
        
        <!-- Left Section (Dynamic Project Information) -->
        <div class="flex flex-col justify-between bg-white p-6 rounded-lg md:w-[26%] w-full">
          <h2 class="text-2xl font-comfortaabold mb-4">{{ currentCaseStudy.title }}</h2>
          <div class="text-lg">
            <div class="mb-2">
              <span class="font-comfortaalight">Client:</span> {{ currentCaseStudy.client }}
            </div>
            <div class="mb-2">
              <span class="font-comfortaabold ">Year:</span> {{ currentCaseStudy.year }}
            </div>
            <div class="mb-2">
              <span class="font-comfortaabold">Platform:</span> {{ currentCaseStudy.platform }}
            </div>
          </div>
        </div>
  
        <!-- Middle Section (Image) -->
        <div class="flex-1 w-full relative rounded-2xl z-10">
          <img :src="currentCaseStudy.imageUrl" alt="Project Screenshot" class="rounded-lg h-full">
        </div>
  
        <!-- Right Section (Project Description) -->
        <div class="flex flex-col justify-between w-full md:w-[40%] bg-white p-2 rounded-lg shadow-d">
          <div class="z-10">
            <div class="flex w-[50%] h-[8rem] gap-4">
              <!-- Smaller Images -->
              <img
                v-for="(image, index) in currentCaseStudy.smallImages"
                :key="index"
                @click="selectCaseStudy(index)"
                :src="image"
                class="rounded-[2rem] cursor-pointer"
                alt="Case Study Image">
            </div>
  
            <!-- Project Description -->
            <h3 class="text-xl font-comfortaabold mb-4 relative">PROJECT DESCRIPTION</h3>
            <p class="mb-4">{{ currentCaseStudy.description }}</p>
          </div>
  
          <!-- Tags Section -->
          <div class="grid grid-cols-3 mt-4">
            <span v-for="(tag, index) in currentCaseStudy.tags" :key="index" class="bg-white px-0.5 py-1 text-xs font-comfortaalight rounded-full">
              <span class="bg-[#FF9500] rounded-full px-[5px] py-[1px] mr-2">&nbsp;</span>{{ tag }}
            </span>
          </div>
        </div>
      </div>
  
      <!-- Toolbar (Next/Previous Buttons) -->
      <div class="flex justify-center mt-6 space-x-4">
        <button @click="prevCaseStudy" class="px-4 py-2 bg-blue-500 text-white rounded-md">Previous</button>
        <button @click="nextCaseStudy" class="px-4 py-2 bg-blue-500 text-white rounded-md">Next</button>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue';
  
  // Array of case studies
  const caseStudies = ref([
    {
      title: "WA Country Health Services",
      client: "WA Country Health Services",
      year: "2023",
      platform: "Web Design",
      imageUrl: "https://thumbs.dreamstime.com/blog/2011/06/vertical-horizontal-photos-69796-image19575639.jpg",
      description: "Zyrous designed and developed a property management system for the Western Australian Country Health Services, streamlining operations and enhancing efficiency. The system featured intuitive user interfaces and robust data management capabilities to efficiently oversee properties across their extensive network.",
      smallImages: [
        "https://www.shutterstock.com/shutterstock/photos/2432595867/display_1500/stock-photo-businessman-analysis-enterprise-data-management-by-ai-artificial-intelligence-technology-business-2432595867.jpg",
        "https://www.shutterstock.com/shutterstock/photos/2420665051/display_1500/stock-photo-a-diverse-team-of-colleagues-enthusiastically-engages-with-content-on-a-laptop-capturing-a-2420665051.jpg"
      ],
      tags: ["APP DESIGN", "UX DESIGN", "END USER"]
    },
    {
      title: "AI Data Management Platform",
      client: "Tech Innovators",
      year: "2024",
      platform: "AI & Data",
      imageUrl: "https://assets.isu.pub/document-structure/230323110934-5489403394ba856bb804e102a057c157/v1/7f761712e58521d06991619d716da7fe.jpeg",
      description: "This case study involves creating a sophisticated AI-powered platform that assists businesses in data management and analytics. The platform is designed to be scalable, with a focus on user experience and data security.",
      smallImages: [
        "https://www.shutterstock.com/shutterstock/photos/2432595867/display_1500/stock-photo-businessman-analysis-enterprise-data-management-by-ai-artificial-intelligence-technology-business-2432595867.jpg",
        "https://thumbs.dreamstime.com/blog/2011/06/vertical-horizontal-photos-69796-image19575639.jpg"
      ],
      tags: ["AI", "DATA ANALYTICS", "SCALABLE PLATFORM"]
    }
  ]);
  
  // Reactive state to track the selected case study
  const selectedCaseStudyIndex = ref(0);
  
  // Computed property to get the current case study
  const currentCaseStudy = computed(() => caseStudies.value[selectedCaseStudyIndex.value]);
  
  // Function to select a case study by index
  function selectCaseStudy(index) {
    selectedCaseStudyIndex.value = index;
  }
  
  // Function to go to the next case study
  function nextCaseStudy() {
    if (selectedCaseStudyIndex.value < caseStudies.value.length - 1) {
      selectedCaseStudyIndex.value++;
    } else {
      selectedCaseStudyIndex.value = 0; // Loop back to the first case study
    }
  }
  
  // Function to go to the previous case study
  function prevCaseStudy() {
    if (selectedCaseStudyIndex.value > 0) {
      selectedCaseStudyIndex.value--;
    } else {
      selectedCaseStudyIndex.value = caseStudies.value.length - 1; // Loop back to the last case study
    }
  }
  </script>
  
  <style>
  /* Add any additional styles if necessary */
  </style>
  