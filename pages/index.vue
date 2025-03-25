<template>
  <div class="px-[3%] bg-[#1878B9] relative">
    <section class="sticky top-5 z-50 px-[1%]">
      <HomeNavBarNavbar :currentSection="currentSection" />
    </section>
    <section class="hero-section section" data-section="Home">
      <HomeHeroSectionHomePage />
    </section>
    <section class="Case-Studies section" data-section="Case Studies">
      <CaseStudies />
    </section>
    <section class="How-It-Works section" data-section="How It Works">
      <HowItWorks />
    </section>
    <section class="Our-Team section" data-section="Our team">
      <OurTeam />
    </section>
    <section class="Contact-us section" data-section="Contact-Us">
      <ContactUs />
    </section>
  </div>
</template>

 <script setup>
import { ref, onMounted } from 'vue';
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
import CaseStudies from '~/components/Pages/caseStudies.vue';
import HowItWorks from '~/components/Pages/how-It-Works.vue';
import OurTeam from '~/components/Pages/ourTeam.vue';
import ContactUs from '~/components/Pages/contactUs.vue';
gsap.registerPlugin(ScrollTrigger);

const currentSection = ref('Home');

onMounted(() => {
  const navbarHeight = document.querySelector('section.sticky').offsetHeight;

  gsap.utils.toArray(".section").forEach((section) => {
    ScrollTrigger.create({
      trigger: section,
      start: `top+=${navbarHeight} ${navbarHeight}px`, 
      end: "bottom top",
      onEnter: () => currentSection.value = section.dataset.section,
      onEnterBack: () => currentSection.value = section.dataset.section,
    });
  });



  gsap.utils.toArray(".section").forEach((section) => {
    gsap.fromTo(
      section,
      { opacity: 1, scale: 1, zIndex: 1 },
      {
        opacity: 0,
        scale: 0.8,
        zIndex: 0,
        ease: "power1.inOut",
        scrollTrigger: {
          trigger: section,
          start: `top+=${navbarHeight} ${navbarHeight}px`, 
          end: "bottom 20%",
          scrub: true,
          pin: true,
          pinSpacing: false,
          onEnter: (self) => {
            self.animation.delay(2); 
          },
        },
      }
    );
  });
});
</script>

<style scoped>
.section {
  @apply h-screen flex items-center justify-center;
}
</style> 
