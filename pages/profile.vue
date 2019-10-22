<template>
  <div class="container">
    <main>
      <p style="margin: 16px;">1992年生まれのプログラマです</p>
      <p>使える言語：Java、Kotlin、Javascript、C#、PHP、Swift、Ruby、Python、Dart、Go</p>
      <p>ライブラリ：RxJava、Android Room、Vue.js、Angular、Flutter</p>
    </main>
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

main {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

main p {
  margin: 4px;
}

footer {
  padding: 16px;
  color: #cccccc;
}

footer a {
  color: #cccccc;
}
</style>
