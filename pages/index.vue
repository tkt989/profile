<template>
  <div class="container">
    <site
      v-for="site in sites"
      :key="site.url"
      :title="site.title"
      :url="site.url"
    ></site>
  </div>
</template>

<script>
import Site from '~/components/Site.vue'

export default {
  data: () => {
    return {
      sites: [
        {
          title: "Blog",
          url: "https://blog.info.tkt989"
        },
        {
          title: "Twitter",
          url: "https://twitter.com/tkt989_dev"
        },
        {
          title: "Github",
          url: "https://github.com/tkt989"
        }
      ]
    }
  },
  components: {
    Site
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
