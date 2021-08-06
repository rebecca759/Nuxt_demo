<template>
    <div class="container">
        <article>
            <h1 class="title">{{post.title}}</h1>
            <p>{{post.content}}</p>
        </article>
    </div>
</template>

<script>
export default {
    name: 'NuxtCourseId',

    data() {
        return {
            id: this.$route.params.id,

        }
    },

    head() {
        return {
            title: this.post.title,
            meta: [
                {name: 'twitter:title',content: this.post.title},
                {name: 'twitter:description', content: this.post.content},
                {name: 'twitter:card',content: 'summary_large_image'}
            ]
        }
    }, 

    computed: {
        post() {
            return this.$store.state.posts.all.find(post => post.id === this.id)
        },

        relatedPosts() {
            return this.$route.state.posts.all.filter(post => post.id !== this.id)
        }
    }
    
};
</script>

<style scoped>

</style>