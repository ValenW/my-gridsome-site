<template>
<Layout>
  <div>
    <h1>Post {{ $page.post.id }}</h1>
    <h2>{{ $page.post.title }}</h2>
    <p>{{ $page.post.content }}</p>
  </div>
</Layout>
</template>

<page-query>
query($id: ID!) {
  post(id: $id) {
    id
    title
    content
  }
}
</page-query>

<script>
export default {
 name: 'Post',
  data() {
    return {

    }
  },
  components: {},
  watch: {},
  mounted() {},
  methods: {}
}
</script>

<style scoped>

</style>