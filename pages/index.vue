<template>
  <div class="p-4">
    <Hero />
    <Articles v-bind:data="getArticleList.items" />
  </div>
</template>

<script>
import allArticle from '../apollo/queries/allArticle.gql'

export default {
  apollo: {
    getArticleList: {
      prefetch: true,
      query: allArticle
    }
  },
};
</script>
