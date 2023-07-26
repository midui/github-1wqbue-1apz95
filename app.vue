<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup lang="ts">
const visible = ref(false);

watch(visible, (newVisible, oldVisible) => {
  useHead({
    bodyAttrs: {
      style: newVisible ? 'overflow: hidden;' : '',
    },
  });
});
</script>
