<template>
	<div class="pages-news flex flex-col items-center justify-center">
		<FeaturesWaitlistBoxContainer class="w-1/3 mt-6">
			<div class="bg-white shadow-md rounded-lg overflow-hidden max-w-[33.33vw] mx-auto my-12" v-if="randomArticle">
				<img :src="randomArticle.image" class="w-full h-60 object-cover mb-6" />
				<div class="p-6">
					<h1 class="text-xl font-semibold text-center text-gray-800 mb-6">{{ randomArticle.title }}</h1>
					<p class="text-gray-600 mt-4 p-4">{{ randomArticle.description }}</p>
				</div>
			</div>
		</FeaturesWaitlistBoxContainer>
		
	</div>
</template>
<script setup>
definePageMeta({
	layout: 'kfc',
	ssr: false
})

const randomArticle = ref(null)

//获取文章数
const  count = await queryContent('kfc').count();
console.log('count: ', count)

//随机获取文章
const  randomIndex = Math.floor(Math.random() * count);
console.log('randomIndex', randomIndex)


const articles = await queryContent('kfc').limit(1).skip(randomIndex).find()

randomArticle.value = articles[0]

</script>
