<template>
  <div class="p-5">
    <h1 class="text-center text-3xl my-8">
      Posts
    </h1>
    <div class="grid gap-2 w-full">
      <BlogPostCard
          v-for="{ _path: slug, title, description, cover } in posts"
          :key="slug"
          :title="title"
          :description="description"
          :slug="slug"
          :cover-src="cover"
      />
    </div>
  </div>
</template>

<script setup>
const { data: posts } = await useAsyncData('posts', () => queryContent('/blog/').sort({date: -1}).find())
</script>