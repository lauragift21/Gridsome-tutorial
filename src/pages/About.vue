<template>
  <Layout>
    <h1>Email Information</h1>
    <ul>
      <li v-for="(item, index) in $page.allFaker.edges" :key="index">
        {{item.node.author}}
        <img :src="item.node.avatar.src">
        <p>{{item.node.email.src}}</p>
      </li>
    </ul>
  </Layout>
</template>

<page-query>
{
 allFaker(perPage: 4){
  edges {
    node {
      id
      author
      email
      avatar
    }
  }
}
}
</page-query>

<script>
export default {};
</script>
