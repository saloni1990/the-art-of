<template>
    <div class="min-h-screen text-center mx-auto bg-gray-200">
        <div class="bg-white">
            <Header />
        <div class="max-w-4xl px-4 mx-auto content">
            <h1 class="mb-8 italic">{{page.title}}</h1>
            <div class="w-full flex justify-center pb-4">
                <cld-image :publicId="`/interactive_agents/${page.pageImage}`"  width="500" crop="fill" />
            </div>
            <div v-html="parseMarkdown(page.body)" class="px-4 "></div>

        </div>
        <Footer />
        </div>
        
    </div>
</template>


<script>

import marked from 'marked'
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
// import cloudinary from 'cloudinary-core';
// const cloudinaryCore = new cloudinary.Cloudinary({cloud_name: 'smartav'});


export default {
  data() {
    return {
      index: 0
    }
  },

  components: {
    Header,
    Footer
  },
  async asyncData({ params, payload }) {
    if (payload) return { page: payload }
    else
      return {
        page: await require(`~/assets/content/pages/about/about.json`)
      }
  },
  methods: {
    parseMarkdown(content) {
      if (content) {
        return marked(content)
      }
    },
    // cloudinarySrc(publicId) {
    //   return cloudinaryCore.url(`/interactive_agents/${publicId}`, { width: 800, height:800, crop: "fit"});
    // }
  },
}
</script>

<style></style>
