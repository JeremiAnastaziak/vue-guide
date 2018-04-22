<template>
  <div id="app">
    <Wrapper tag-name="section">
      <Playground />
      <Post v-for="post in posts" v-bind:text="post.text" v-bind:key="post.text" />
    </Wrapper>
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import Playground from './components/Playground.vue'
  import Post from './components/Post.vue'
  import Wrapper from './components/Wrapper.vue';

  export default {
    name: 'app',
    data: () => ({
      posts: [{
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
      Post,
      Wrapper
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
