<template>
  <div class="links">
    <nuxt-link v-for="post in posts" :to="{name: 'posts-id', params: {id: post.id}}" :key="post.id" class="button--grey">
      {{ post.title }}
      <br>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  computed: {
    posts() {
      return this.$store.state.posts.all;
    }
  },

  head() {
    return {
      title: 'Home Page',
      meta: [
                {name: 'twitter:title',content: 'Next Fundamentals by Vue'},
                {name: 'twitter:description', content: 'Nuxt + vue school'},
                {name: 'twitter:card',content: 'summary_large_image'}
            ] 
    }
  }
};
</script>
