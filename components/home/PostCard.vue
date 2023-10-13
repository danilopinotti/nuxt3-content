<template>
  <div class="card card-compact w-full bg-base-100 shadow-xl">
  <figure><img :src="coverSrc" :alt="description" class="h-40 object-cover"/></figure>
  <div class="card-body">
    <h2 class="card-title">{{ title }}</h2>
    <p>{{ description }}</p>
    <div class="card-actions justify-end">
      <NuxtLink :to="slug">
        <button class="btn btn-link">Ver mais</button>
      </NuxtLink>
    </div>
  </div>
</div>
</template>

<script setup>
defineProps(['title', 'description', 'slug', 'coverSrc'])
</script>