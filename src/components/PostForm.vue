<template>
  <form @submit.prevent>
    <h4>Create post</h4>
    <input 
      v-model="post.title"
      class="input"
      type="text"
      placeholder="Title"
    >
    <input 
      v-model="post.body"
      class="input"
      type="text"
      placeholder="Body"
    >
    <style-button
      @click="createPost"
      class="form__btn"
    >
      Create
    </style-button>
  </form>
</template>

<script>
import StyleButton from './ui/StyleButton'
export default {
  components: {StyleButton},
  data() {
    return {
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post);
      this.post = {
        title: '',
        body: '',
      }
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
}

.input {
  margin-top: 15px;
  padding: 10px 15px;
  border: 1px solid teal;
  width: 100%;
}

.form__btn {
  margin-top: 15px;
  align-self: flex-end;
}
</style>