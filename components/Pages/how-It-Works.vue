<template>
  <section class="w-[95%] h-[70%] py-6  pb-0">
    <div class="bg-white rounded-3xl px-3 py-4">
      <div class="flex flex-col md:flex-row justify-between">
        <!-- Left Section -->
        <div
          class="flex flex-col md:w-[45%] w-full items-start text-center pt-[8%] mx-auto"
        >
          <div class="flex mb-3">
            <!-- Column 1 -->
            <div class="flex justify-center items-center text-center">
              <h1
                @click="
                  openDetail({
                    title: 'How',
                    bgColor: '#A9DFFF',
                    imgSrc: '../assets/sliderimg1.webp',
                    description: 'Description for How',
                  })
                "
                class="rounded-xl p-3 font-comfortaabold text-3xl bg-gradient-to-r from-[#A9DFFF] to-[#72C5FD] text-black m-1 transition-all duration-500 transform hover:scale-105 hover:shadow-lg"
              >
                How
              </h1>
            </div>
            <!-- Column 2 -->
            <div class="flex justify-center items-center text-center">
              <h1
                @click="
                  openDetail({
                    title: 'It',
                    bgColor: '#1A1A1A',
                    imgSrc: '../assets/sliderimg1.webp',
                    description: 'Description for It',
                  })
                "
                class="rounded-xl px-[50%] py-[30%] font-comfortaabold text-3xl bg-gradient-to-r from-[#1A1A1A] to-[#2E2E2E] text-white ml-5 transition-all duration-500 transform hover:scale-105 hover:shadow-lg"
              >
                It
              </h1>
            </div>
          </div>
          <!-- Column spanning both columns -->
          <div class="flex justify-center items-center text-center mb-2">
            <h1
              @click="
                openDetail({
                  title: 'Works',
                  bgColor: '#1A1A1A',
                  imgSrc: '../assets/sliderimg1.webp',
                  description: 'Description for Works',
                })
              "
              class="rounded-xl p-3 font-comfortaabold text-3xl bg-gradient-to-r from-[#1A1A1A] to-[#2E2E2E] text-white m-1 transition-all duration-500 transform hover:scale-105 hover:shadow-lg"
            >
              Works
            </h1>
          </div>
          <!-- Text Section -->
          <div class="mt-5 w-[80%] text-start">
            <p class="text-[3vw] lg:text-[1.2vw] font-semibold">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci
              reiciendis deleniti qui ducimus ab odio ipsam, quibusdam repellat
              aut numquam consectetur odit excepturi dolor veniam praesentium.
            </p>
          </div>
        </div>
        <!-- Right Section with Stats -->
        <div
          class="md:w-1/2 w-full flex justify-center md:justify-end mt-2 md:mt-0 relative aspect-[1]"
        >
          <!-- Large Circle -->
          <div
            class="aspect-[1] absolute top-[0%] right-[40%] bg-gradient-to-r from-[#ddeec9] via-[#c9e7a5] to-[#eaf3df] text-green-800 w-[45%] rounded-full text-center shadow-lg flex flex-col justify-center items-center"
          >
            <p class="text-[3vw] md:text-[2.7vw] font-comfortaabold p-[4%]">User-Centric Design</p>
            <div
              class="absolute top-[10%] left-[10%] bg-white border-4 border-[#ddeec9] rounded-es-xl rounded-se-xl  overflow-hidden px-[5%]"
            >
              <button
                @click="
                  openDetail({
                    title: 'User-Centric Design',
                    bgColor: '#EAF3DF',
                    imgSrc: '../assets/sliderimg1.webp',
                    description: 'Description for User-Centric Design',
                  })
                "
                class="md:text-[1.5vw] text-[2.5vw] "
              >
                Click Me
              </button>
            </div>
          </div>
          <!-- Other Circles -->
          <div
            class="aspect-[1] absolute bottom-[8%] right-[8%] bg-gradient-to-r from-[#e6eefa] via-[#c7d1df] to-[#6796a3] text-blue-800 w-[50%] rounded-full text-center shadow-lg flex flex-col justify-center items-center"
          >
            <p class="text-[3vw] md:text-[3vw] font-comfortaabold">Life Time Support</p>
            <div
              class="absolute top-8 right-0 bg-white border-4 px-[10%] py-[0%] border-[#e6eefa] rounded-es-xl rounded-se-xl overflow-hidden"
            >
              <button
                @click="
                  openDetail({
                    title: 'Life Time Support',
                    bgColor: '#E6EEFA',
                    imgSrc: '../assets/sliderimg1.webp',
                    description: 'Description for Life Time Support',
                  })
                "
                class="md:text-[1.5vw] text-[2.5vw]"
              >
                Click Me
              </button>
            </div>
          </div>
          <div
            class="aspect-[1] absolute left-[0%] top-[55%] bg-gradient-to-r from-[#dee9ec] via-[#b4cbd2] to-[#dee9ec] text-purple-800 w-[30%] rounded-full text-center shadow-lg flex flex-col justify-center items-center"
          >
            <p class="text-[3vw] md:text-[1.5vw] font-comfortaabold">Rigorous Testing</p>
            <div
              class="absolute top-5 -right-5 px-2 bg-white border-4 border-[#dee9ec] rounded-es-xl rounded-se-xl overflow-hidden"
            >
              <button
                @click="
                  openDetail({
                    title: 'Rigorous Testing',
                    bgColor: '#DEE9EC',
                    imgSrc: '../assets/sliderimg1.webp',
                    description: 'Description for Rigorous Testing',
                  })
                "
                class="md:text-[1.5vw] text-[2.5vw] cursor-pointer"
              >
                Click Me
              </button>
            </div>
          </div>
          <div
            class="aspect-[1] absolute right-[0%] top-[10%] bg-gradient-to-r from-[#ebe9f0] via-[#d3d0dc] to-[#ebe9f0] text-gray-800 w-[30%] rounded-full text-center shadow-lg flex flex-col justify-center items-center"
          >
            <p class="text-[3vw] md:text-[1.5vw] font-comfortaabold">
              Define Clear <br />
              Objectives
            </p>
            <div
              class="absolute -top-0 right-0 bg-white border-4 border-[#ebe9f0] rounded-es-xl rounded-se-xl overflow-hidden"
            >
              <button
                @click="
                  openDetail({
                    title: 'Define Clear Objectives',
                    bgColor: '#EBE9F0',
                    imgSrc: '../assets/sliderimg1.webp',
                    description: 'Description for Define Clear Objectives',
                  })
                "
                class="md:text-[1.5vw] text-[2.5vw]"
              >
                Click Me
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Popup -->
    <div
      v-if="selectedItem"
      class="fixed inset-10 flex items-center justify-center bg-opacity-5 z-20"
    >
      <div
        :style="{ backgroundColor: selectedItem.bgColor }"
        class="relative bg-white rounded-3xl shadow-2xl p-8 w-[85%] h-[85%] flex flex-col md:flex-row"
      >
        <button
          @click="closeDetail"
          class="absolute top-4 right-4 text-black font-bold text-2xl"
        >
          &times;
        </button>
        <img
          :src="selectedItem.imgSrc"
          :alt="selectedItem.title"
          class="w-[45%] md:w-[35%] h-2/3 object-cover rounded-3xl mt-10 md:mb-0 md:mr-4"
        />
        <div
          class="flex flex-col justify-center pl-[4rem] h-full w-full md:w-1/2"
        >
          <h1 class="text-2xl font-bold mb-4">{{ selectedItem.title }}</h1>
          <p class="text-lg">{{ selectedItem.description }}</p>
          <img
            src="../assets/sliderimg1.webp"
            class="w-[70%] h-[70%]"
            alt="Image"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      selectedItem: null,
    };
  },
  methods: {
    openDetail(item) {
      this.selectedItem = item;
    },
    closeDetail() {
      this.selectedItem = null;
    },
  },
};
</script>

<style scoped>
/* Add any specific styling here */
</style>
