<template>
  <nav :class="mobile ? 'flex flex-col space-y-4' : 'hidden md:flex items-center space-x-8'">
    <NuxtLink 
      v-for="item in navItems" 
      :key="item.name"
      :to="item.href"
      class="text-gray-700 hover:text-blue-600 font-medium transition-colors"
      active-class="text-blue-600"
    >
      {{ item.name }}
    </NuxtLink>
  </nav>
</template>

<script setup>
defineProps({
  mobile: {
    type: Boolean,
    default: false
  }
})

const navItems = [
  { name: 'Home', href: '/' },
  { name: 'About', href: '/about' },
  { name: 'Services', href: '/services' },
  { name: 'Contact', href: '/contact' }
]
</script>