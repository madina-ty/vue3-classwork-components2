<template>
<div class="container">
<InputComp @send-post="addPost"/>
<div class="d-flex flex-column" v-for="(post, i) in posts" :key="i">
  <PostComp>{{ post.text }}</PostComp>
</div>
</div>
</template>

<script>
import InputComp from './components/InputComp.vue';
import PostComp from './components/PostComp.vue';

export default {
  name: 'App',
  components: {
   InputComp,
   PostComp,
  },

  data: () => {
    return {
     posts: []
    }
  },
  methods: {
    addPost(text) {
      this.posts.push({
        text: text,
        likes: 0,
      })
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: aliceblue;
  padding-top: 60p;
  text-align: center;
  color: #2c3e50;
  padding-bottom: 100px;
}
</style>
