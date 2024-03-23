<script setup>
definePageMeta({
  title: "Josiah | Full-stack Developer",
  description: "I create accessable and delightful web applications.",
});

useHead({
  titleTemplate: "",
});

const route = useRoute();

useSeoMeta({
  ogTitle: () => route.meta.title,
  twitterTitle: () => route.meta.title,
});
</script>

<template>
  <div>
    <h1>Hello World!</h1>
  </div>
</template>
