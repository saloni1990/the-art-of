<template>
<div>
    <div v-for="blog in blog"
          :key="blog.slug"
          class="flex items-center">
        {{blog.title}}
      </div>
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
</div>
</template>

<script>
export default {
   computed: {
  blog() {
    return this.$store.state.blog
  }
  },
}
</script>
