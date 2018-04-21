<template>
  <div id="app">
    <Playground />
    <Post
      v-for="post in posts"
      v-bind:text="post.text"
    />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Playground from './components/Playground.vue'
import Post from './components/Post.vue'

export default {
  name: 'app',
  data: () => ({
    posts: [
      {
        text: 'New article'
      },
      {
        text: 'Another article'
      }
    ]
  }),
  components: {
    HelloWorld,
    Playground,
    Post
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
