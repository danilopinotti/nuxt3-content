<template>
  <div class="p-5">
    <div class="mb-4">
      <button class="btn btn-primary" @click="$router.back()">Voltar</button>
    </div>
    <article class="prose lg:prose-xl">
      <ContentDoc />
    </article>
  </div>
</template>
