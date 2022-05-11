<template>
  <div class="app">
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostList from './components/PostList';
import PostForm from './components/PostForm';

export default {
  components: {PostForm, PostList},
  data() {
    return {
      posts: [
        {id: 1, title: 'title 1', body: 'desc 1'},
        {id: 2, title: 'title 2', body: 'desc 2'},
        {id: 3, title: 'title 3', body: 'desc 3'},
        {id: 4, title: 'title 4', body: 'desc 4'},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
    },
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>
