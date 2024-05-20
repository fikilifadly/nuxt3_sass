<template>
	<div class="hero_banner">
		<div class="cta-section">
			<h1 class="hero-title">One More Friend</h1>
			<h2 class="hero-secondary">Thousands More Fun!</h2>
			<p class="hero-paragraph">
				Having a pet means you have more joy, a new friend, a happy person who will always be with you to have fun. We have 200+ different pets that can meet your needs!
			</p>
			<div class="cta-button">
				<button class="cta-primary">View Intro <img src="../assets/icons/Play_Circle.png" alt="btn-play" loading="lazy" class="icon" /></button>
				<button class="cta-secondary">Explore Now</button>
			</div>
		</div>
		<div class="img-wrapper">
			<LazyNuxtImg src="/hero-banner.webp" alt="hero-image" loading="lazy" class="hero-img" />
		</div>
	</div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../assets/css/variables.scss";

.hero_banner {
	background-color: $primary-color;
	height: 794px;
	width: 100%;
	border-bottom-left-radius: 20px;
	border-bottom-right-radius: 20px;
	position: relative;
	overflow: hidden;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: center;

	.cta-section {
		display: flex;
		flex-direction: column;
		padding: 0 16px;
		color: white;
		padding-top: 150px;

		.hero-title {
			@include main-font;
		}

		.hero-secondary {
			@include secondary-font;
		}

		.hero-paragraph {
			@include paragraph-font;
			margin-bottom: 20px;
			margin-top: 10px;
		}
	}

	.cta-button {
		display: flex;
		flex-wrap: wrap;
		gap: 15px;
		button {
			border-radius: 50px;
			font-size: 16px;
			min-width: 163px;
			max-width: 163px;
			height: 48px;
			padding: 0 28px;
		}
		.icon {
			width: 24px;
			height: 24px;
		}

		.cta-primary {
			background-color: transparent;
			border: 1.5px solid $darkblue-color;
			color: $darkblue-color;
			display: flex;
			align-items: center;
			justify-content: space-between;
		}

		.cta-secondary {
			background-color: $darkblue-color;
			color: white;
			border: unset;
		}
	}

	.img-wrapper {
		width: 100%;
		height: 386px;
		position: relative;
		z-index: 2;
		.hero-img {
			width: 100%;
			height: 100%;
			object-fit: cover;
			z-index: 2;
		}
		&:before {
			content: "";
			position: absolute;
			z-index: -2;
			width: 500px;
			height: 500px;
			transform: rotate(5deg);
			border-radius: 48px;
			top: 112px;
			left: 55px;
			background-color: $darkblue-color;
		}
		&:after {
			content: "";
			position: absolute;
			z-index: -1;
			width: 500px;
			height: 500px;
			transform: rotate(23deg);
			border-radius: 48px;
			background-color: $secondary-color;
			top: 85px;
			left: 100px;
		}
	}

	@media screen and (min-width: 768px) {
		height: 695px;
		border-bottom-left-radius: 40px;
		border-bottom-right-radius: 40px;
		padding: 0 5%;
		display: grid;
		grid-template-columns: 1fr 1fr;
		padding-top: 95px;
		grid: 1;

		.cta-section {
			padding-top: unset;
			width: 100%;
		}

		.img-wrapper {
			width: 100%;
			height: 600px;
			&:before {
				width: 635px;
				height: 635px;
				border-radius: 99px;
				transform: rotate(9deg);
				top: 233px;
				left: 16px;
			}
			&:after {
				width: 610px;
				height: 695px;
				border-radius: 99px;
				transform: rotate(23deg);
				top: 195px;
				left: 51px;
			}
		}
	}
}
</style>
