<template>
	<NuxtLayout>
		<template v-slot:content>
			<ContentDoc />
		</template>
		
		<template v-slot:footer>
			112233
		</template>
	</NuxtLayout>
</template>
<script setup>
definePageMeta({
	layout: 'control', // 指定使用 admin 布局	
})
</script>