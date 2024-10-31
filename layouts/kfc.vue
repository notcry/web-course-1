<template>
	 <div>
		<ControlHeader />
		 <slot />
		<ControlFooter />
	 </div>
</template>
<style scoped>
/* 确保 <nuxt /> 有足够的空间展示页面内容 */
div {
  min-height: 100vh;
}
</style>