<template>
  <div>
    <section class="hero is-primary is-medium">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column ">
              <figure class="image is-128x128">
                <img :src="content.img" alt="header-image"/>
              </figure>
            </div>
            <div class="column is-four-fifths">
              <h1 class="title">
                {{ content.title }}
              </h1>
              <h2 class="subtitle">{{ content.description }}</h2>
            </div>
          </div>

        </div>
      </div>
    </section>
  <section class="section">
    <div class="container">
        <nuxt-content :document="content"/>
    </div>
  </section>
  </div>
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

