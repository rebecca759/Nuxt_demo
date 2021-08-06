<template>
    <div class="container">
        <article>
            <h1 class="title">What is Balut?</h1>
            <p>If someone placed balut on your plate, you might think they were serving you a hardboiled egg. That is, until you cracked it open and a fully intact</p>
        </article>
    </div>
</template>

<script>
export default {
    name: 'NuxtCoursePost',
};
</script>

<style scoped>
    .container {
        display: flex;
        justify-content: space-between;
        line-height: 1.5;
    }

    article * {
        margin-bottom: 1rem;
    }

    aside {
        min-width: 280px;
        max-width: 280px;
    }

</style>