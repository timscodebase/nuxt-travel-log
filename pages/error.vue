<script lang="ts" setup>
const route = useRoute();
const error = route.query.error as string || "An unknown error occurred";
</script>

<template>
  <div class="card bg-base-300 container mx-auto mt-4 min-h-72 text-center flex flex-col items-center gap-4">
    <div role="alert" class="alert alert-error min-w-1/2 text-center">
      <span>Oh Darn!! {{ error }}</span>
    </div>
    <NuxtLink to="/" class="btn btn-accent">
      Go Back Home
      <Icon name="tabler:arrow-left" size="24" />
    </NuxtLink>
  </div>
</template>
