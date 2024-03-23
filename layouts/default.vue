<script setup>
useHead({
  titleTemplate: "%s | Josiah",
});

const route = useRoute();

const serverMeta = {
  ogImage: "/og-image.png",
  twitterImage: "/og-image.png",
  ogType: "website",
  ogLocale: "en_US",
  twitterCard: "summary",
  twitterCreator: "@josiah136",
};

useSeoMeta({
  title: () => route.meta.title,
  description: () => route.meta.description,
  ogTitle: () => `${route.meta.title} | Josiah`,
  twitterTitle: () => `${route.meta.title} | Josiah`,
  ogDescription: () => route.meta.description,
  twitterDescription: () => route.meta.description,
  ogUrl: () => `https://josiahrose.me${route.path}`,
  ...serverMeta,
  // Load ServerMeta
});
</script>

<template>
  <div class="bg-gray-900 min-h-screen flex flex-col">
    <slot />
  </div>
</template>
