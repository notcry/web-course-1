<template>
<div class="container mx-auto">
	<FeaturesWaitlistBoxContainer class="my-6">
		<div class="grid grid-cols-3 gap-4">
			<ContentList path="/news" v-slot="{ list }">
				<div v-for="article in list" :key="article._path" class="bg-white shadow-md rounded-lg overflow-hidden">
					<NuxtLink :to="article._path" class="block hover:opacity-75 transition-opacity duration-300">
						<img v-if="article.image" :src="article.image" class="w-full h-48 object-cover">
						<div class="p-4">
							<h2 class="text-xl font-semibold text-blue-600 mb-4">{{ article.title }}</h2>
							<p class="text-gray-700 mb-6">{{ article.description }}</p>
						</div>
					</NuxtLink>
				</div>		
			</ContentList>
		</div>
	</FeaturesWaitlistBoxContainer>
</div>
</template>
<script setup>
definePageMeta({
	layout : 'news'
})
</script>

<style scoped>
.pages-news {
	min-height: calc(100vh - 100px);
}
</style>