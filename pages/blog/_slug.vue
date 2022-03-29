<template>
  <article>
    
    
    <nav id="header" class="fixed w-full z-10 top-0">

      <div class="w-full md:max-w-4xl mx-auto flex flex-wrap items-center justify-between mt-0 py-3">

        <div class="pl-4">
          <a class="text-gray-900 text-base no-underline hover:no-underline font-extrabold text-xl" href="#">
            {{ article.category }}
          </a>
        </div>
        
      </div>
    </nav>
    
    <div class="container w-full md:max-w-3xl mx-auto pt-20 min-h-screen">

      <div class="w-full px-4 md:px-6 text-xl text-gray-800 leading-normal" style="font-family:Georgia,serif;">

        <div class="font-sans">
          <p class="text-base md:text-sm text-green-500 font-bold">&lt; <a href="#" class="text-base md:text-sm text-green-500 font-bold no-underline hover:underline">BACK TO BLOG</a></p>
              <h1 class="font-bold font-sans break-normal text-gray-900 pt-6 pb-2 text-3xl md:text-4xl">{{ article.title }}</h1>
              <p class="text-sm md:text-base font-normal text-gray-600">Published {{ article.published }}</p>
        </div>

        <nuxt-content :document="article" class="py-6" />

      </div>

      <hr class="border-b-2 border-gray-400 mb-8 mx-4">

    </div>

    <footer class="bg-white border-t border-gray-400 shadow">
      <div class="container max-w-4xl mx-auto flex py-8">

        <div class="w-full mx-auto flex flex-wrap">
          <div class="flex w-full md:w-1/2 ">
            <div class="px-8">
              <h3 class="font-bold text-gray-900">About</h3>
              <p class="py-4 text-gray-600 text-sm">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas vel mi ut felis tempus commodo nec id erat. Suspendisse consectetur dapibus velit ut lacinia.
              </p>
            </div>
          </div>

          <div class="flex w-full md:w-1/2">
            <div class="px-8">
              <h3 class="font-bold text-gray-900">Social</h3>
              <ul class="list-reset items-center text-sm pt-3">
                <li>
                  <a class="inline-block text-gray-600 no-underline hover:text-gray-900 hover:text-underline py-1" href="#">Add social link</a>
                </li>
                <li>
                  <a class="inline-block text-gray-600 no-underline hover:text-gray-900 hover:text-underline py-1" href="#">Add social link</a>
                </li>
                <li>
                  <a class="inline-block text-gray-600 no-underline hover:text-gray-900 hover:text-underline py-1" href="#">Add social link</a>
                </li>
              </ul>
            </div>
          </div>
        </div>



      </div>
    </footer>

  </article>
</template>


<script>
  export default {
    async asyncData({ $content, params }) {

      const article = await $content('articles', params.slug).fetch()

      return { article }
    },
    head() {
      return {
        title: this.article.title,
        //meta: [
          // hid is used as unique identifier. Do not use `vmid` for it as it will not work
          //{
            //hid: 'description',
            //name: 'description',
            //content: 'My custom description'
          //}
        //]
      }
    }
  }
</script>
