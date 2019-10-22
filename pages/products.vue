<template>
  <div class="container">
    <div class="sites">
      <site
        v-for="site in sites"
        :key="site.url"
        :title="site.title"
        :url="site.url"
      ></site>
    </div>

    <footer>Powered by <a href="https://nuxtjs.org/">Nuxt.js</a></footer>
  </div>
</template>

<script>
import Site from '~/components/Site.vue'

export default {
  data: () => {
    return {
      sites: [
        {
          title: "Google Play",
          url: "https://play.google.com/store/apps/developer?id=tkt989"
        },
        {
          title: "App Store",
          url: "https://apps.apple.com/jp/developer/takashi-tomoto/id1367155936"
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
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.sites {
  flex-grow: 1;
  display: flex;
  align-items: center;
}

footer {
  padding: 16px;
  color: #cccccc;
}

footer a {
  color: #cccccc;
}
</style>
