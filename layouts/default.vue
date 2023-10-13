<template>
  <div class="flex flex-col min-h-screen bg-base-200">
    <Navbar/>
    <div class="flex-grow w-full h-full max-w-screen-2xl mx-auto">
      <slot/>
    </div>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Navbar from "~/components/layout/Navbar.vue";
import Footer from "~/components/layout/Footer.vue";
</script>
