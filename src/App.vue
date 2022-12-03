<template>
  <section class="bg-[#171717] text-[#A3ABB2] font-Poppins font-medium text-sm sm:text-base sm:leading-8">
    <div class="max-w-[797px] m-auto px-5 pt-10 pb-10">
      <!-- Profile -->
      <div class="w-full flex flex-col sm:flex-row items-center justify-center gap-[40px]">
        <div class="p-1 w-[215px] bg-[#A3ABB2] rounded-full">
          <img :src="`./PP.jpg`" alt="" class="w-full rounded-full ">
        </div>
        <div class="flex flex-col items-center sm:items-start">
          <h1 class="text-[32px] sm:text-[46px] text-white leading-[76px]">Radyan Bintang</h1>
          <h2 class="sm:mt-2">Junior Web Developer</h2>
          <div class="media flex gap-6 mt-6">
            <a v-for="media in medias" :key="media" :href="`${media.ref}`"><i :class="`${media.link}`"
                class="text-3xl text-[36px]"></i></a>
          </div>
        </div>
      </div>
      <!-- Description -->
      <div class="mt-7 sm:mt-12 md:w-[634px] flex justify-center gap- sm:gap-[90px] py-5 m-auto">
        <div v-for="profile in profiles" :key="profile" class="">
          <h1 align="center" class="text-base sm:text-2xl">{{ profile.p1 }}</h1>
          <h1 align="center">{{ profile.p2 }}</h1>
        </div>
      </div>
      <!-- CV Contact button -->
      <div class="mt-8 sm:w-[618px] flex justify-between m-auto">
        <a href="https://drive.google.com/file/d/1ACfXB9ZZkEVDf0WjpgsbvgDLq7h924Lk/view">
          <button
            class="bg-white hover:bg-white/90 duration-100 text-[#171717] w-[158px] sm:w-[290px] h-[44px] sm:h-16 rounded-[10px]">Download
            CV<i class="fa-solid fa-file-arrow-down ml-2"></i></button>

        </a>
        <a href="mailto:radyan6661@gmail.com ">
          <button class="bg-[#242424] w-[158px] sm:w-[290px] h-[44px] sm:h-16 rounded-[10px]">Contact Me</button>
        </a>
      </div>
      <!-- Tabs button -->
      <div class="w-full h-[96px] mt-12 sm:mt-20 bg-[#242424] rounded-[20px] p-4 flex justify-between">
        <button class="h-16 w-[350px] bg-[#171717] rounded-[10px]">Portfolio</button>
        <button v-on:click="clicked = !clicked" v-bind:class="{ 'bg-[#171717]': clicked, 'bg-transparent': !clicked }"
          class="h-16 w-[350px] rounded-[10px]">Skills</button>
      </div>
      <!-- Portfolio -->
      <div class="mt-8 w-full grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Project -->
        <div v-for="portfolio in portfolios" :key="portfolio" class="bg-[#242424] rounded-2xl relative overflow-hidden border-white border-2">
          <div class="group rounded-t-2xl h-[226px] overflow-hidden relative border-white border-b-2">
            <img :src="`${portfolio.img}`" alt="" class="">
          </div>
          <div class=" w-full p-4 font-normal text-base">
            <h1 class="text-2xl font-medium text-white">{{ portfolio.name }}</h1>
            <h1 class="mt-3">Built with : {{ portfolio.built }}</h1>
            <a :href="`${portfolio.link}`" class="relative rounded-2xl">
              <button class="mt-3 underline hover:text-white ">View </button>
            </a>
          </div>
        </div>
      </div>
        <!-- Small Projects -->
        <h1 class="mt-10"> <span class="text-white">#</span> Small-projects</h1>
        <div class="mt-8 w-full grid grid-cols-1 md:grid-cols-2 gap-8">
        <div v-for="project in projects" :key="project" class="bg-[#242424] rounded-2xl relative overflow-hidden border-white border-2">
          <div class="group rounded-t-2xl h-[226px] overflow-hidden relative border-white border-b-2">
            <img :src="`${project.img}`" alt="" class="">
          </div>
          <div class=" w-full p-4 font-normal text-base">
            <h1 class="text-2xl font-medium text-white">{{ project.name }}</h1>
            <h1 class="mt-3">Built with : {{ project.built }}</h1>
            <a :href="`${project.link}`" class="relative rounded-2xl">
              <button class="mt-3 underline hover:text-white ">View </button>
            </a>
          </div>
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
      { link: 'fa-brands fa-github', ref: 'https://github.com/rdynxyz' },
      { link: 'fa-brands fa-instagram', ref: 'https://www.instagram.com/radyanbintang/' },
      { link: 'fa-brands fa-linkedin', ref: '' },
    ]
    let profiles = [
      { p1: '1', p2: 'Year of work experience' },
      { p1: '5+', p2: 'Completed web apps' },
      { p1: '5+', p2: 'Small projects' },
    ]
    let portfolios = [
      { img: 'Salty.jpg', link: 'https://salty-rdynxyz.vercel.app/', name: 'Salty - Travel Website', built: 'Vue Tailwind' },
      { img: 'Eunoia.jpg', link: 'https://rdynxyz.github.io/eunoia/', name: 'Eunoia - Service Website', built: 'HTML JS Tailwind' },
      { img: 'Real State.jpg', link: 'https://realstate-rdynxyz.vercel.app', name: 'Reis - Real State Website', built: 'HTML JS Tailwind' },
      { img: 'Portfolio.jpg', link: 'https://portfolio-rdynxyz.vercel.app', name: 'Portfolio - You’re using it rn', built: 'Vue Tailwind' },
    ]
    let projects = [
      { img: 'tic-tac-toe.jpg', link: 'https://tic-tac-toe-rdynxyz.vercel.app/', name: 'Tic Tac Toe Game', built: 'Vue Tailwind' },
      { img: 'Real State.jpg', link: 'https://simple-calculator-rdynxyz.vercel.app', name: 'Simple Calculator', built: 'HTML JS' },
    ]
    return { medias, profiles, portfolios, projects }
  }
}
</script>

<style>

</style>