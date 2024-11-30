<template>
  <!-- <UContainer> -->
  <nav
    class="flex items-center justify-between py-4 bg-white shadow-md"
    style="height: 70px"
  >
    <!-- Left-hand side: Home and Shop Icons -->
    <div class="flex items-center space-x-4">
      <!-- <nuxt-link
        to="/"
        class="text-gray-700 hover:text-indigo-500 flex items-center space-x-2"
      >
      

        <UButton
          icon="i-heroicons-home"
          size="sm"
          color="white"
          circle
          variant="link"
        />
      </nuxt-link> -->
      <!-- <nuxt-link
        to="/shop"
        class="text-gray-700 hover:text-indigo-500 flex items-center space-x-2"
      >
        <UButton
          icon="i-heroicons:shopping-cart-solid"
          size="sm"
          color="white"
          circle
          variant="link"
        />
      </nuxt-link> -->
      <nuxt-link to="/" class="text-xl font-bold text-indigo-600">
        <!-- <img src="/public/favicon.ico" alt="Logo" class="h-10 w-auto" /> -->
        <img
          src="/public/logo.png"
          alt="Logo"
          class="h-20 w-auto"
        />
      </nuxt-link>
    </div>

    <!-- Center: Logo -->
    <div>
     
    </div>

    <!-- Right-hand side: Cart and Profile Icons -->
    <div class="flex items-center space-x-4">
      <!-- <nuxt-link to="/cart" class="text-gray-700 hover:text-indigo-500">
        <UButton
          icon="i-heroicons:building-storefront-20-solid"
          size="sm"
          color="white"
          circle
          variant="link"
        />
      </nuxt-link> -->
      <nuxt-link to="/login" class="text-gray-700 hover:text-indigo-500">
        <UButton
          icon="heroicons:arrow-left-end-on-rectangle"
          size="sm"
          color="white"
          circle
          variant="link"
          class="pr-3"
        />
      </nuxt-link>
    </div>
  </nav>
  <!-- </UContainer> -->
</template>
  
  <script setup>
// Optional: Logic can be added here if needed
</script>
  
  <style scoped>
/* Optional: Add styling for consistent layout */
</style>
  