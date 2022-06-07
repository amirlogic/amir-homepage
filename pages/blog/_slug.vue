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
          <p class="text-base md:text-sm text-green-500 font-bold">&lt; <a href="/blog/" class="text-base md:text-sm text-green-500 font-bold no-underline hover:underline">BACK TO BLOG</a></p>
              <h1 class="font-bold font-sans break-normal text-gray-900 pt-6 pb-2 text-3xl md:text-4xl">{{ article.title }}</h1>
              <p class="text-sm md:text-base font-normal text-gray-600">Published {{ article.published }}</p>
        </div>

        <nuxt-content :document="article" class="py-6" />

      </div>

      <hr class="border-b-2 border-gray-400 mb-8 mx-4">

    </div>

    <Footer></Footer>

  </article>


</template>


<script>
  export default {

    async asyncData({ $content, params, error }) {

      try{
        
        //console.log(`slug: ${params.slug}`);    // DEBUG

        const article = await $content( `articles`, params.slug )
                              .fetch()
                              //.catch((e) => { /${params.dir}
                                //error({ statusCode: 404, message: 'Post not found' })
                              //})

        return { article }

      } catch (err){

        error({

            statusCode: 404,
            message: 'Page could not be found'

          })
      }
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
