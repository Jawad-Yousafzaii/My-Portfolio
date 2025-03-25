<template>
  <section class="w-[94%] h-[90%]">
    <div class="relative">
      <h2 class="text-[4vw] font-bold text-white text-center -mt-[1%]">
        Our Case Studies
      </h2>
      <div
        class="w-[100%] h-[86%] absolute top-[18%] -left-[2%] bg-gradient-to-r from-sky-400 to-blue-600 rounded-xl"
      ></div>
      <swiper
        :slides-per-view="1"
        :loop="true"
        :autoplay="{ delay: 100 }"
        class="rounded-xl"
      >
        <swiper-slide v-for="(caseStudy, index) in caseStudies" :key="index">
          <div class="relative rounded-lg shadow-lg">
            <img
              :src="caseStudy.imgSrc"
              :alt="caseStudy.title"
              class="w-full h-[75vh] object-fill"
            />
            <div
              class="absolute inset-0 bg-gradient-to-t from-black to-transparent p-6 flex flex-col justify-end text-white"
              ref="caseText"
            >
              <h3 class="text-[2.5vw] font-semibold">{{ caseStudy.artist }}</h3>
              <h4 class="text-[4vw] font-bold text-teal-400">
                {{ caseStudy.title }}
              </h4>
              <div class="flex justify-start mt-2 text-[1vw] gap-x-[8%]">
                <div class="text-[1.1vw]">
                  <p>
                    {{ caseStudy.views }}
                  </p>
                </div>
                <div class="text-[1.1vw]">
                  <p>
                    {{ caseStudy.interactions }}
                  </p>
                </div>
                  <div class="text-[1.1vw]">
                    <p>{{ caseStudy.cpm }}</p>
                  </div>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
import { onMounted, ref } from "vue";
import gsap from "gsap";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";
import case1 from '@/assets/casestudy1.webp'
import case2 from '@/assets/casestudy2.webp'

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      caseStudies: [
        {
          artist: "Optimizing Cloud Infrastructure for E-Commerce Growth",
          title: "RetailHub",
          imgSrc: case1, // Replace with actual image paths
          views:
            "RetailHub was struggling with slow website performance and frequent downtimes during peak sales periods.",
          interactions:
            "We restructured their cloud infrastructure by migrating to a more scalable AWS solution, optimizing server performance, and implementing load balancing.",
          cpm: "The website's load time improved by 40%, and downtime during high-traffic events was reduced to zero, resulting in a 30% increase in online sales.",
        },
        {
          artist: "Cybersecurity Overhaul for a Financial Institution",
          title: "SecureBank",
          imgSrc:  case2, // Replace with actual image paths
          views:
            "SecureBank faced increasing threats from cyber-attacks, putting sensitive customer data at risk.",
          interactions:
            "We conducted a thorough security audit, implemented advanced encryption protocols, and established a real-time monitoring system to detect and respond to threats.",
          cpm: " The number of detected security breaches dropped by 80%, and customer confidence in SecureBank's digital services increased significantly.",
        },
        {
          artist: "Custom Software Development for Healthcare Automation",
          title: "HealthSync",
          imgSrc:
            "https://i.pinimg.com/564x/1a/41/9f/1a419f54190588c33755af31c71fadc4.jpg", // Replace with actual image paths
          views:
            "HealthSync needed a custom software solution to streamline patient data management and improve communication between doctors and patients.",
          interactions:
            " We developed a tailored software platform that integrates electronic health records (EHR), appointment scheduling, and telemedicine capabilities.",
          cpm: "HealthSync reported a 50% reduction in administrative tasks and a 25% increase in patient satisfaction due to more efficient and accessible healthcare services.",
        },
      ],
    };
  },
  setup() {
    const caseText = ref([]);

    onMounted(() => {
      caseText.value.forEach((text) => {
        gsap.from(text, {
          duration: 1,
          opacity: 0,
          y: 50,
          ease: "power3.out",
          scrollTrigger: {
            trigger: text,
            start: "top bottom",
          },
        });
      });
    });

    return {
      caseText,
    };
  },
};
</script>

<style scoped></style>
