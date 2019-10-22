<template>
  <div class="container">
    <div class="sites">
      <site
        v-for="site in sites"
        :key="site.url"
        :title="site.title"
        :url="site.url"
        :to="site.to"
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
          title: "Profile",
          to: "profile"
        },
        {
          title: "Blog",
          url: "https://blog.tkt989.info"
        },
        {
          title: "Twitter",
          url: "https://twitter.com/tkt989_dev"
        },
        {
          title: "Github",
          url: "https://github.com/tkt989"
        },
        {
          title: "Products",
          to: "products"
        },
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
  flex-direction: row;
  align-items: center;
}

@media only screen and (orientation: portrait) {
  .sites {
    flex-direction: column;
  }
}

footer {
  padding: 16px;
  color: #cccccc;
}

footer a {
  color: #cccccc;
}
</style>
