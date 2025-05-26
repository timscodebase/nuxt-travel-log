<script lang="ts" setup>
const colorMode = useColorMode();

const isDark = computed({
  get() {
    return colorMode.value === "business";
  },
  set(value) {
    colorMode.preference = value ? "business" : "corporate";
  },
});
</script>

<template>
  <label class="swap swap-rotate mx-4">
    <!-- this hidden checkbox controls the state -->
    <input v-model="isDark" type="checkbox">

    <!-- sun icon -->
    <Icon name="tabler:sun-filled" size="24" class="swap-on" />

    <!-- moon icon -->
    <Icon name="tabler:moon-filled" size="24" class="swap-off" />
  </label>
</template>
