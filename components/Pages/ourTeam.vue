<template>
  <div class="w-[95%] h-[94%] flex justify-center items-center bg-white rounded-3xl scale-[94%]">
    <div class="container flex flex-col justify-around items-center w-full h-full rounded-lg">
      <!-- First Row -->
      <div class="flex justify-center items-center w-full gap-x-[8%] ">
        <div v-for="(person, index) in firstRow" :key="index" class="flex justify-center items-center">
          <div v-if="person.isButton" @click="selectCategory(person.label)"
            class="bg-[#1878B9] w-[10vw] h-[10vw] text-[2vw] p-2 -mt-[10%] text-white py-2 px-4 rounded-full font-comfortaabold flex items-center justify-center cursor-pointer">
            {{ person.label }}
          </div>
          <div style="box-shadow: 2px 15px 22px 23px rgba(204, 204, 204, 0.59)" v-else
            class="flex items-center justify-center rounded-full transition duration-300" :class="{
              'opacity-20':
                selectedCategory !== 'Meet Our Team' &&
                selectedCategory !== person.category,
              'opacity-100':
                selectedCategory === 'Meet Our Team' ||
                selectedCategory === person.category,
            }">
            <img :src="person.image" :class="[
              'rounded-full object-cover shadow-lg ',
              index === 0 || index === 2 ? 'w-[11vw]' : 'w-[9vw]',
            ]" />
          </div>
        </div>
      </div>

      <!-- Second Row -->
      <div class="flex justify-center items-center w-full gap-x-[6%] -mt-[0%] ">
        <div v-for="(item, index) in secondRow" :key="index" class="flex justify-center items-center">
          <div v-if="item.isButton" @click="selectCategory(item.label)" :class="[
            'text-center rounded-full flex items-center justify-center p-2 cursor-pointer',
            index === 2
              ? 'w-[12vw] h-[12vw] bg-[#35495E] text-white mt-[2.5%] font-comfortaabold text-[2vw]'
              : index === 4
                ? 'w-[11vw] h-[11vw] bg-[#3B8070] text-white font-comfortaabold text-[2vw] -mr-[15%] -mt-[15%]'
                : 'w-[11vw] h-[11vw] bg-[#AEDDFF] text-black font-comfortaabold text-[2vw] -ml-[10%] -mt-[10%]',
          ]">
            {{ item.label }}
          </div>

          <div v-else class="flex items-center justify-center -mt-[20%] rounded-full transition duration-300" :class="{
            'opacity-50':
              selectedCategory !== 'Meet Our Team' &&
              selectedCategory !== item.category,
            'opacity-100':
              selectedCategory === 'Meet Our Team' ||
              selectedCategory === item.category,
          }" style="box-shadow: 2px 15px 22px 23px rgba(204, 204, 204, 0.59)">
            <img :src="item.image" :alt="`Person ${index + 4}`" class="rounded-full object-cover w-[12vw] h-[12vw]" />
          </div>
        </div>
      </div>

      <!-- Third Row -->
      <div class="flex justify-center items-center w-full gap-[10%] -mt-[2%] ">
        <div style="box-shadow: 0px 10px 37px 6px rgba(204, 204, 204, 0.65)" v-for="(image, index) in thirdRow"
          :key="index" :class="[
            'flex justify-center items-center rounded-full transition duration-300',
            index === 0
              ? 'w-[12vw]  ml-[2%] -mt-[4%]'
              : index === 1
                ? 'w-[11vw] h-[11vw]  mt-[3%]'
                : 'w-[9.5vw] h-[9.5vw]',
            selectedCategory !== 'Meet Our Team' &&
              selectedCategory !== image.category
              ? 'opacity-0'
              : 'opacity-100',
          ]">
          <img :src="image.src" :alt="`Person ${index + 6}`"
            class="rounded-full object-cover shadow-lg w-full h-full" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamSection",
  data() {
    return {
      selectedCategory: "Meet Our Team",
      firstRow: [
        {
          image:
            "https://i.pinimg.com/564x/bc/73/54/bc73543e1700c51cf7f4fbd929dde49a.jpg",
          category: "CEO",
        },
        { isButton: true, label: "CEO" },
        {
          image:
            "https://i.pinimg.com/564x/6c/ef/3c/6cef3c6f70607cdbe6e27fe1e49dd60d.jpg",
          category: "Backend Team",
        },
        {
          image:
            "https://i.pinimg.com/564x/ff/c5/b9/ffc5b9bf4e5274a8c8dc42b95b326fd2.jpg",
          category: "Frontend Team",
        },
      ],

      secondRow: [
        {
          isButton: true,
          label: "Frontend Team",
        },
        {
          image:
            "https://i.pinimg.com/236x/a2/3c/24/a23c2402885d815dfc6a588c6bef488e.jpg",
          category: "Frontend Team",
        },
        {
          isButton: true,
          label: "Meet Our Team",
        },
        {
          image:
            "https://i.pinimg.com/564x/99/8f/41/998f41fc4c63e69c06b99a6e03629815.jpg",
          category: "Backend Team",
        },
        {
          isButton: true,
          label: "Backend Team",
        },
      ],
      thirdRow: [
        {
          src: "https://i.pinimg.com/736x/6f/34/ac/6f34ac1f864b6ce51d1139bfd6df0060.jpg",
          category: "Frontend Team",
        },
        {
          src: "https://i.pinimg.com/564x/99/8f/41/998f41fc4c63e69c06b99a6e03629815.jpg",
          category: "Backend Team",
        },
        {
          src: "https://i.pinimg.com/564x/0b/5c/d0/0b5cd0b51e431bbac4dffa331a3cbed5.jpg",
          category: "Frontend Team",
        },
        {
          src: "https://i.pinimg.com/564x/99/8f/41/998f41fc4c63e69c06b99a6e03629815.jpg",
          category: "Backend Team",
        },
      ],
    };
  },
  methods: {
    selectCategory(category) {
      this.selectedCategory = category;
    },
  },
};
</script>

<style scoped></style>
