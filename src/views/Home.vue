<template>
	<div class="home-view">
		<img class="logo" alt="NA-J logo" :src="logo">
		<div class="description">
			Strona w budowie...
		</div>
	</div>
</template>

<script>
import logo from '@/Assets/Images/logo/logo.svg'

export default {
	name: 'Home',
	data() {
		return {
			logo
		}
	}
}
</script>

<style lang="scss" scoped>
	.home-view {
		width: 100%;
		height: calc(100% - 70px);
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		font-weight: normal;
		.logo {
			width: 450px;
			max-width: 80%;
			animation: bounce 0.5s both;
		}
		.description {
			font-size: 25px;
			/* font-weight: bold; */
			margin: 30px 0 0 0;
			animation: elation 0.3s 0.5s both;
			&::before {
				content: '';
				position: absolute;
				bottom: 0;
				left: 50%;
				transform: translateX(-50%);
				width: 30%;
				height: 3px;
				background-color: $secondary;
				border-radius: 3px;
			}
		}
	}
</style>
