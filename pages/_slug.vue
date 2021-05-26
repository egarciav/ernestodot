<template>
    <article>
        <nuxt-content :document="article" />
    </article>
</template>

<script>
export default {
    async asyncData({ $content, params}) {
        const article = await $content('blog', params.slug).fetch();

        return { article }
    }
}
</script>

<style>
article {
  display: block;
  margin: 0 auto;
  padding: 90px 30px;
  max-width: 800px;
  line-height: 22px;
}
</style>