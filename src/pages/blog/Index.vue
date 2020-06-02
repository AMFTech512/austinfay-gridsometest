<template>
    <Layout>
        <h1>Blog Posts</h1>
        <ul>
            <li v-for="blogPost in $static.posts.edges" :key="blogPost.node.id">
                <g-link :to="blogPost.node.path">{{ blogPost.node.title }}</g-link>
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
        path
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