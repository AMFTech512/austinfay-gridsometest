<template>
    <Layout>
        <h1>Blog Posts</h1>
        <ul>
            <li v-for="blogPost in $static.posts.edges" :key="blogPost.id">
                <g-link :to="`/blog/${blogPost.node.id}`">{{ blogPost.node.title }}</g-link>
            </li>
        </ul>
    </Layout>
</template>

<static-query>
query{
  posts: allBlogPost{
    edges{
      node{
        id
        title
        description
        content
      }
    }
  }
}
</static-query>

<style>

</style>