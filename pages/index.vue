<template>
  <div>
    <h1 class="text-center text-3xl my-8">
      Bem vindo ao Blog do Danilo!!!
    </h1>
    <img src="/images/dev.jpg" alt="dev-img" class="object-cover w-full h-56">
    <div class="p-5 mt-8">
      <h2 class="text-xl font-light text-center mb-5">Últimas postagens</h2>
      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-2">
        <PostCard
            v-for="{ _path: slug, title, description, cover } in posts"
            :key="slug"
            :title="title"
            :description="description"
            :slug="slug"
            :cover-src="cover"
        />
      </div>
      <div class="flex justify-center mt-4">
        <NuxtLink to="/blog">
          <button class="btn btn-primary">Ver todos os posts</button>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import PostCard from "~/components/home/PostCard.vue";

const {data: posts} = await useAsyncData('posts', () => queryContent('/blog/')
    .sort({date: -1})
    .limit(4)
    .find())
</script>