<template>
  <header class="bg-white shadow-sm fixed w-full top-0 z-50">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
      <div class="flex items-center">
        <!-- <NuxtImg src="/logo.png" alt="Logo" class="h-8 w-auto" /> -->
      </div>
      
      <Navigation />
      
      <div class="hidden md:flex items-center space-x-4">
        <Button variant="outline">Login</Button>
        <Button>Get Started</Button>
      </div>
      
      <!-- Mobile menu button -->
      <button 
        @click="toggleMobileMenu"
        class="md:hidden p-2"
      >
        <Icon name="heroicons:bars-3" class="h-6 w-6" />
      </button>
    </nav>
    
    <!-- Mobile menu -->
    <div v-show="mobileMenuOpen" class="md:hidden bg-white border-t">
      <div class="px-4 py-4 space-y-4">
        <Navigation mobile />
        <div class="flex flex-col space-y-2">
          <Button variant="outline" class="w-full">Login</Button>
          <Button class="w-full">Get Started</Button>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import Navigation from './Navigation.vue'
import Button from '~/components/ui/Button.vue'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}
</script>