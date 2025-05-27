<script lang="ts" setup>
const authStore = useAuthStore();
await authStore.init();
</script>

<template>
  <div class="flex min-h-screen flex-col">
    <main>
      <AppNavBar />
      <slot />
    </main>
  </div>
</template>
