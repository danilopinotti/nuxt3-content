<template>
  <div class="navbar bg-base-100">
    <div class="flex-1">
      <NuxtLink to="/" class="btn btn-ghost normal-case text-xl">My Blog</NuxtLink>
    </div>
    <div class="flex-none">
      <div class="menu menu-horizontal px-1 flex gap-6">
        <NuxtLink to="/">Início</NuxtLink>
        <NuxtLink to="/blog">Blog</NuxtLink>
      </div>
    </div>
  </div>
</template>