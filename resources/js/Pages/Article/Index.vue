<script setup>
import { defineAsyncComponent } from 'vue';

const MainLayout = defineAsyncComponent(() => import('../../Layouts/Main.vue'));

const { articles } = defineProps({
  articles: {
    type: Object,
    required: true
  }
})

console.log(articles)
</script>

<template>
  <MainLayout>
    <section>
      <h2>Read our latest articles</h2>

      <article v-for="(article, key) in articles" :key="key">
        <div>
          <!-- <img src="/images/kinsta-logo.png" alt="Article thumbnail" /> -->
        </div>

        <h3>{{ article.title }}</h3>
        <p>
          {{ article.excerpt }}
        </p>

        <a href="#">Read more</a>
      </article>
    </section>
  </MainLayout>
</template>