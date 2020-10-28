<template>
  <Layout>
    <div>
      <h1>Posts</h1>
      <ul>
        <li v-for="{ node } in $page.posts.edges" :key="node.id">
          <g-link>{{ node.title }}</g-link>
        </li>
      </ul>
    </div>
  </Layout>
</template>

<page-query>
query {
  posts: allPost {
    edges {
      node {
        id
        title
        content
      }
    }
  }
}
</page-query>

<script>
export default {
  name: "Posts",
  data() {
    return {};
  },
  components: {},
  watch: {},
  mounted() {},
  methods: {},
};
</script>

<style scoped>
</style>