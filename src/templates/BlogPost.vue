<template>
    <Layout>
        <h1>{{ $page.blogPost.title }}</h1>
        <p v-html="$page.blogPost.content"></p>
    </Layout>
  
</template>

<page-query>
query ($id: ID!) {
  blogPost(id: $id) {
    path
    id
    title
    description
    content
  }
}
</page-query>

<style>

</style>