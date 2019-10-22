<template>
  <div>
    <a
      v-if="url"
      :href="url"
    >{{title.toUpperCase()}}</a>
    <nuxt-link
      v-if="to"
      :to="to"
    >{{title.toUpperCase()}}</nuxt-link>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    url: String,
    to: String
  }
}
</script>

<style scoped>
a {
  display: inline-block;
  font-family: "Source Code Pro", monospace;
  text-decoration: none;
  font-weight: bold;
  background-color: white;
  color: black;
  padding: 16px;
  margin: 16px;
  transition: filter 300ms;
  filter: invert(100%);
  font-size: 1.3rem;
  max-width: 300px;
}

a::first-letter {
  font-size: 2.6rem;
}

a:hover {
  filter: invert(0%);
}
</style>
