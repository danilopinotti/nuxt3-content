<template>
  <div class="card lg:card-side bg-base-100 shadow">
    <figure><img :src="coverSrc" alt="Movie" class="object-contain h-40 w-72"/></figure>
    <div class="card-body">
      <h2 class="card-title">{{ title }}</h2>
      <p>{{ description }}</p>
      <div class="card-actions justify-end">
        <NuxtLink :to="slug">
          <button class="btn btn-primary">Ver</button>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps(['title', 'description', 'slug', 'coverSrc'])
</script>