<template>

  <home>
    <nav id="header" class="fixed w-full z-10 top-0">

      <div class="w-full md:max-w-4xl mx-auto flex flex-wrap items-center justify-between mt-0 py-3">

          <div class="pl-4">
            <a class="text-gray-900 text-base no-underline hover:no-underline font-extrabold text-xl" href="#">
              home
            </a>
          </div>
          
      </div>
    </nav>

    <div class="container w-full md:max-w-3xl mx-auto pt-20 min-h-screen">

      <div class="w-full px-4 md:px-6 text-xl text-gray-800 leading-normal" style="font-family:Georgia,serif;">

          <div class="font-sans">
            
                <h1 class="font-bold font-sans break-normal text-gray-900 pt-6 pb-2 text-3xl md:text-4xl"></h1>
                <p class="text-sm md:text-base font-normal text-gray-600">Published </p>
          </div>

          <nuxt-content :document="article" class="py-6" />

      </div>

      <hr class="border-b-2 border-gray-400 mb-8 mx-4">

    </div>

  </home>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>
