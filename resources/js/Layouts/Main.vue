<script setup>

import { defineAsyncComponent } from 'vue';

const Header = defineAsyncComponent(() => import('./Header.vue'));
const Footer = defineAsyncComponent(() => import('./Footer.vue'));

</script>

<template>
  <Header />

  <main>
    <slot />
  </main>

  <Footer />
</template>