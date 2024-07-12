<template>
  <h3>New Post</h3>
  <form @submit.prevent="submit">
    <input 
      v-model="newPost.title"
      placeholder="Title"
    />
    <br />
    <textarea cols="50" rows="10" v-model="newPost.content" placeholder="Your post" />
    <br />
    <button>Submit</button>
  </form>
</template>
<script>

export default {
  methods: {
    submit() {
      this.$emit('createPost', {
        
      })
      const id = postStore.posts.value.length + 1
      postStore.addPost({
        id,
        title: newPost.title,
        content: newPost.content
      })
      this.$router.push('/posts/${id}')

    }
  }

  // setup() {
  //   const postStore = usePosts()
  //   const router = useRouter()

  //   const newPost = reactive({
  //     title: '',
  //     content: '',
  //   })

  //   const submit = () => {
  //     const id = postStore.posts.value.length + 1
  //     postStore.addPost({
  //       id,
  //       title: newPost.title,
  //       content: newPost.content
  //     })
  //     router.push('/posts/${id}')
  //   }

  //   return {
  //     newPost,
  //     submit
  //   }
  // }
}
</script>

<style scoped>
</style>