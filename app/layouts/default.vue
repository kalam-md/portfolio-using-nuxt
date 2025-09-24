<template>
  <div class="min-h-screen flex flex-col">
    <main class="flex-1">
      <slot />
    </main>
  </div>
</template>

<script setup>
import Header from '~/components/layout/Header.vue'
</script>