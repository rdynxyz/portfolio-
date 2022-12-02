<template>
  <section class="bg-[#171717] text-[#A3ABB2] font-Poppins font-medium text-sm sm:text-[22px]">
    <div class="max-w-[797px] m-auto px-5 pt-10 pb-10">
      <!-- header -->
      <div class="w-full flex flex-col sm:flex-row items-center justify-center gap-[40px]">
        <div class="p-1 w-[215px] bg-white rounded-full">
          <img :src="`./PP.jpg`" alt="" class="w-full rounded-full ">
        </div>
        <div class="flex flex-col items-center sm:items-start">
          <h1 class="text-[32px] sm:text-[46px] text-white leading-[76px]">Radyan Bintang</h1>
          <h2 class="mt-2">Junior Web Developer</h2>
          <div class="media flex gap-6 mt-6">
            <a v-for="media in medias" :key="media" href=""><i :class="`${media.link}`"
                class="text-3xl text-[36px]"></i></a>
          </div>
        </div>
      </div>
      <!-- askldj -->
      <div class="mt-7 sm:mt-12 md:w-[634px] flex justify-center gap- sm:gap-[90px] py-5 m-auto">
        <div v-for="profile in profiles" :key="profile" class="">
          <h1 align="center" class="text-2xl">{{ profile.p1 }}</h1>
          <h1 align="center">{{ profile.p2 }}</h1>
        </div>
      </div>
      <!-- button -->
      <div class="mt-7 sm:mt-12 sm:w-[618px] flex justify-between m-auto">
        <button class="bg-white text-[#171717] w-[158px] sm:w-[290px] h-[44px] sm:h-[80px] rounded-[10px]">Download CV</button>
        <button class="bg-[#242424] w-[158px] sm:w-[290px] h-[44px] sm:h-[80px] rounded-[10px]">Contact Me</button>
      </div>
      <!-- Tabs button -->
      <div class="w-full h-[116px] mt-12 sm:mt-20 bg-[#242424] rounded-[20px] p-[18px] flex justify-between">
        <button class="h-full w-[350px] bg-[#171717] rounded-[10px]">Portfolio</button>
        <button v-on:click="clicked = !clicked" v-bind:class="{ 'bg-[#171717]': clicked, 'bg-transparent': !clicked }"
          class="h-full w-[350px] rounded-[10px]">Skills</button>
      </div>
      <!-- portfolio -->
      <div class="mt-7 sm:mt-12 w-full grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="rounded-2xl h-[226px] overflow-hidden">
          <a href="https://6388c2695b2ccc172e721076--rdyn.netlify.app/">
            <img :src="`./Salty.jpg`" alt="" class="rounded-2xl">
          </a>
        </div>
        <div class="rounded-2xl h-[226px] overflow-hidden">
          <a href="https://6388c2695b2ccc172e721076--rdyn.netlify.app/">
            <img :src="`./Salty.jpg`" alt="" class="rounded-2xl">
          </a>
        </div>
        <div class="rounded-2xl h-[226px] overflow-hidden">
          <a href="https://6388c2695b2ccc172e721076--rdyn.netlify.app/">
            <img :src="`./Salty.jpg`" alt="" class="rounded-2xl">
          </a>
        </div>
        <div class="rounded-2xl h-[226px] overflow-hidden">
          <a href="https://6388c2695b2ccc172e721076--rdyn.netlify.app/">
            <img :src="`./Salty.jpg`" alt="" class="rounded-2xl">
          </a>
        </div>
      </div>
      <!-- Credit -->
      <h1 class="text-center mt-32">© Radyan Bintang. 2022 All rigths reserved</h1>
    </div>
  </section>
</template>

<script>
export default {
  setup() {
    let medias = [
      { link: 'fa-brands fa-github' },
      { link: 'fa-brands fa-instagram' },
      { link: 'fa-brands fa-linkedin' },
    ]
    let profiles = [
      { p1: '1 years', p2: 'Years of work experience' },
      { p1: '50+', p2: 'Completed projects' },
      { p1: '20+', p2: 'Satisfied customers' },
    ]
    return { medias, profiles }
  }
}
</script>

<style>

</style>