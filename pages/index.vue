<template>

  <home>
    <nav id="header" class="fixed w-full z-10 top-0">

      <div class="w-full md:max-w-4xl mx-auto flex flex-wrap items-center justify-between mt-0 py-3">

          <div class="pl-4">
            <a class="text-gray-900 text-base no-underline hover:no-underline font-extrabold text-xl" href="#">
              Amir's homepage
            </a>
          </div>
          
      </div>
    </nav>

    <div class="container w-full md:max-w-3xl mx-auto pt-20 min-h-screen">

      <div class="w-full px-4 md:px-6 text-xl text-gray-800 leading-normal" style="font-family:Georgia,serif;">

          <div class="">
            
                <h1 class="font-bold font-sans break-normal text-gray-900 pt-6 pb-2 text-3xl md:text-4xl">Pharmacist &amp; Programmer</h1>
                
                <p class="mt-6">I studied Pharmacy for 5 years, then I spent 4 more years doing a residency program in Medical Laboratory Science,
                  and since the early years of my undergraduate studies, I learned myself programming, and I understood that code has an fantastic power.
                  During the last decade, social media apps have changed our lives, thanks to web technologies, and the digital transformation is coming to healthcare, 
                  although the process is a little bit slower, but some concepts are now a reality: Telemedecine is already a thing, and artificial intelligence is being used in image analysis as well as drug discovery.
                </p>

                <p class="mt-6"></p>

          </div>

          <div><a href="/blog/tech">Tech</a> - <a href="/blog/med">Med</a> - <a href="/blog/misc">Misc</a></div>

      </div>

    </div>

    <footer class="bg-white border-t border-gray-400 shadow">
      <div class="container max-w-4xl mx-auto flex py-8">

        <div class="w-full mx-auto flex flex-wrap">

          <div class="flex w-full md:w-1/2 ">
            <div class="px-8">

              <h3 class="font-bold text-gray-900">Amir Hachaichi</h3>
              <p class="py-4 text-gray-600 text-sm">
                Copyright 2022
              </p>

            </div>
          </div>

          <div class="flex w-full md:w-1/2">
            <div class="px-8">

              <h3 class="font-bold text-gray-900">Social</h3>

              <ul class="list-reset items-center text-sm pt-3">

                <li>
                  <a class="inline-block text-gray-600 no-underline hover:text-gray-900 hover:text-underline py-1" href="https://www.linkedin.com/in/amirhac/" target="_blank">LinkedIn</a>
                </li>
                <li>
                  <a class="inline-block text-gray-600 no-underline hover:text-gray-900 hover:text-underline py-1" href="https://amir-hac.medium.com" target="_blank">Medium</a>
                </li>
                <li>
                  <a class="inline-block text-gray-600 no-underline hover:text-gray-900 hover:text-underline py-1" href="https://github.com/amirlogic" target="_blank">GitHub</a>
                </li>
                
              </ul>

            </div>
          </div>

        </div>

      </div>
    </footer>

  </home>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>
