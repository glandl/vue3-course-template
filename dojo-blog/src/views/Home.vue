<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :post="posts" />
    <button>toggle posts</button>
  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from '@vue/reactivity'

export default {
  name: 'Home',
  components: { PostList },
  setup() {
    const posts = ref([
      { title: 'welcome to the blog', body: 'Lorem ipsum', id: 1},
      { title: 'top 5 CSS tips', body: 'Lorem ipsum', id: 2},
    ])
    const showPosts = ref(true)
    return { posts, showPosts }
  }
}
</script>
