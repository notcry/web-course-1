<template>
	<!-- Right: Login Form -->
	<div class="lg:p-36 md:p-52 sm:20 p-8 w-full lg:w-1/2">
		<h1 class="text-2xl font-semibold mb-4">登录</h1>
		<form action="#" method="POST">
			<!-- Username Input -->
			<div class="mb-4 bg-sky-100">
				<label for="username" class="block text-gray-600">用户名</label>
				<input type="text" id="username" name="username"
					class="w-full border border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:border-blue-500"
					autocomplete="off">
			</div>
			<!-- Password Input -->
			<div class="mb-4">
				<label for="password" class="block text-gray-800">密码</label>
				<input type="password" id="password" name="password"
					class="w-full border border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:border-blue-500"
					autocomplete="off">
			</div>
			<!-- Remember Me Checkbox -->
			<div class="mb-4 flex items-center">
				<input type="checkbox" id="remember" name="remember" class="text-red-500">
				<label for="remember" class="text-green-900 ml-2">记住</label>
			</div>
			<!-- Forgot Password Link -->
			<div class="mb-6 text-blue-500">
				<a href="#" class="hover:underline">忘记密码?</a>
			</div>
			<!-- Login Button -->
			<button type="button" class="bg-red-500 hover:bg-blue-600 text-white font-semibold rounded-md py-2 px-4 w-full" @click="login">登录</button>
		</form>
		<!-- Sign up  Link -->
		<div class="mt-6 text-green-500 text-center">
			<a href="#" class="hover:underline">注册</a>
		</div>
	</div>
</template>
<script>
export default {
	methods: {
		login() {
			// 跳转到首页
			this.$router.push('/control_panel')
		}
	}
}
</script>
