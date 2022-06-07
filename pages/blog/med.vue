<template>
  
  <main>

    <Header></Header>

    <div class="container w-full md:max-w-3xl mx-auto pt-20 min-h-screen">

      <ul>

        <li v-for="post in posts" :key="post.slug">

          <nuxt-link :to="`/blog/${post.slug}`" class="font-mono text-slate-500"> {{ post.title }} </nuxt-link>

        </li>

      </ul>

    </div>
    
    <Footer></Footer>
  

  </main>

  
</template>



<script>

  export default {

      async asyncData({ $content, params, error }) {

        try{

          console.log("med")

          const posts = await $content( { deep: true } )
                              .where( { dir: '/articles/med', category:'med' } )
                              .fetch();

          return { posts, params };

        } catch(err){

          error({

            statusCode: 404,
            message: 'Page could not be found'

          })
        }
      },

    head() {

      return {
        title: "Navigation",
        
      }
    }

  }

</script>