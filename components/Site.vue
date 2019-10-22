<template>
  <a :href="url">{{title}}</a>
</template>

<script>
export default {
  props: {
    title: String,
    url: String
  }
}
</script>

<style>
a {
  display: inline-block;
  font-family: "Source Code Pro", monospace;
  text-decoration: none;
  font-weight: bold;
  background-color: white;
  color: black;
  padding: 16px;
  margin: 16px;
  transition: filter 500ms;
  filter: invert(100%);
}

a:hover {
  filter: invert(0%);
}
</style>
