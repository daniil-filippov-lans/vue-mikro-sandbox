<template>
  <div class="post">
    <div><strong>Title</strong> {{ post.title }}</div>
    <div><strong>Body</strong> {{ post.body }}</div>
    <div class="post__btns">
      <style-button @click="delete">Delete</style-button>
    </div>
  </div>
</template>

<script>
import StyleButton from './ui/StyleButton';
export default {
  components: {StyleButton},
  props: {
    post: {
      type: Object,
      required: true
    }
  },
  methods: {
    delete() {

    }
  }
}
</script>

<style scoped>
.post {
  margin-top: 15px;
  padding: 15px;
  border: 2px solid teal;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.post__btns {

}
</style>