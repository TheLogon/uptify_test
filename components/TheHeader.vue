<template>
	<div class="header">
		<div class="header__inner">
			<div class="header__logo">
				<img src="/images/logo.svg" alt="" />
			</div>
			<button class="header__burger">
				<span></span>
				<span></span>
			</button>
		</div>
	</div>
</template>

<script>
	export default {
		name: "Header",
		async mounted() {
			const data = await $fetch("https://api.coindesk.com/v1/bpi/currentprice.json")
			console.log(data)
		},
	}
</script>

<style lang="scss">
	.header {
		padding: 24px 32px 0 32px;
		position: relative;
		&::before {
			content: "";
			position: absolute;
			top: -900px;
			left: 0;
			z-index: -1;
			width: 1083px;
			height: 1083px;
			border-radius: 1083px;
			background: #0a72d4;
			filter: blur(480px);
		}
		&__inner {
			display: flex;
			justify-content: space-between;
			align-items: center;
		}
		&__logo {
		}
		&__burger {
			width: 64px;
			height: 64px;
			background: linear-gradient(315deg, rgba(51, 123, 190, 0.2) 0%, rgba(0, 0, 0, 0) 100%, rgba(51, 123, 190, 0) 100%), rgba(255, 255, 255, 0.08);
			border-radius: 50%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: flex-end;
			border: none;
			cursor: pointer;
			padding: 0 18px;
			gap: 6px;
			span {
				height: 2px;
				background-color: #fff;
				width: 28px;
				&:nth-child(2) {
					width: 16px;
				}
			}
		}
	}
</style>
