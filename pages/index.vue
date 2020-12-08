<template>
  <section class="section">
    <div class="container">
        <h1 class="title">{{ content.title }}</h1>
        <nuxt-content :document="content"/>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const content = await $content('index').fetch()

    return {
      content
    }
  }
}</script>

