<template>
  <div class="flex flex-wrap">
    <div
      class="p-4 lg:w-1/3 md:w-1/2 sm:w-full"
      v-for="article in data" 
      :key="article._id"
    >
    <p class="text-2xl p-2" v-html="article.title"></p>
      <ix-img
        :src="article.heroimage.path"
        :imgixParams="{ fit: 'crop', ar: '1.8:1' }"
        sizes="(min-width: 1024px) calc(33vw - 60px), (min-width: 768px) calc(50vw - 100px), calc(100vw - 70px)"
        loading="lazy"
      />
      <p class="p-2" v-html="article.content"></p>
    </div>
  </div>
</template>

<script>

export default {
  props: ['data'],
}
</script>

<style></style>
