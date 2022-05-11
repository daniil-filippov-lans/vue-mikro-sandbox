<template>
  <div>
    <h3>List user`s</h3>
    <post-item
      :post="post"
      v-for="post in posts"
      :key="post.id"
    />
  </div>
</template>

<script>
import PostItem from './PostItem'
export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>

</style>