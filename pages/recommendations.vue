<template>
  <div>
    <div class="content">
      <h2>recomendaciones</h2>
      <br />
      <div class="articles">
		  <div class="article" v-for="(article, idx) of articles" :key="idx">
			  <nuxt-link :to="{ name: 'slug', params: { slug: article.slug } }">
				  <div class="article-inner">
						<div class="detail">
							<h3>{{ article.title }}</h3>
							<p>{{ article.description }}</p>
						</div>
				  </div>
			  </nuxt-link>
		  </div>
	  </div>
    </div>
  </div>
</template>

<script>
export default {
	async asyncData({ $content, params }) {
		const articles = await $content('blog', params.slug)
			.only(['title', 'description', 'img', 'slug'])
            .where({ tag: 'rec' })
			.sortBy('createdAt', 'asc')
			.fetch();

		return {
			articles
		}
	}
}
</script>

<style>
.content {
  padding: 75px 15px 0px 15px;
}

.articles {
  margin: 0 auto;
  max-width: 800px;
}

.article {
  margin-bottom: 15px;
}
</style>