<template>
  <div class="">
    <div class="w-full">
      <Header />
      <div class="w-full max-auto pt-2">
        <div class="flex flex-wrap justify-center items-center ">
          <!-- <nuxt-link to="/the-agents" class="px-4 pt-4">
            <cld-image publicId="/interactive_agents/ia-circle_iufla4.jpg" radius="max" width="200" height="200" crop="fill" />
          </nuxt-link> -->
          <div
          v-for="blog in blog"
          :key="blog.slug"
          class="flex items-center"
        >
            <nuxt-link
              class="flex flex-col justify-between h-full px-4 pt-4 "
              :to="'/blog/' + blog.slug"
            >
              <!-- <div class="flex justify-center items-end ">
                <cld-image :publicId="`/interactive_agents/${project.thumbnail}`" radius="max" width="200" height="200" crop="fill" />
              </div> -->
            </nuxt-link>
          </div>
        </div>
      </div>
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  },
  computed: {
  blog() {
    return this.$store.state.blog
  }
  }
  
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
