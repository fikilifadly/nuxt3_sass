<template>
	<div class="icon-wrapper">
		<div class="icon-title">
			<h2>
				Proud to be part of <span>{{ highlight }}</span>
			</h2>

			<button class="hidden-mobile view-more">
				<span>View all our sellers</span>
				<span class="arrow">></span>
			</button>
		</div>

		<div class="icon-gallery">
			<div class="img-wrapper" v-for="(icon, i) in icons" :key="i">
				<NuxtImg :src="icon.icon" :alt="icon" alt="gak sempet kasih obj name" class="icon-image" loading="lazy" />
			</div>
		</div>
		<button class="hidden-desktop view-more">
			<div>
				<span>View More</span>
				<span class="arrow">></span>
			</div>
		</button>
	</div>
</template>

<script setup>
const { title, highlight, icons } = defineProps(["title", "highlight", "icons"]);
</script>

<style lang="scss" scoped>
@import "../assets/css/variables.scss";

.icon-wrapper {
	display: flex;
	flex-direction: column;
	padding: 0 2.5%;
	margin: 35px 0;
	background-color: $white-color;

	.hidden-mobile {
		display: none;
	}

	.icon-title {
		margin-bottom: 10px;
		h2 {
			line-height: 20px;
			font-size: 16px;
			font-weight: 100;

			span {
				font-size: 20px;
				color: $darkblue-color;
				font-weight: 600;
			}
		}
	}

	.icon-gallery {
		display: grid;
		grid-template-columns: repeat(3, auto);
		justify-items: center;
		gap: 10px;
		margin-bottom: 20px;
		.img-wrapper {
			width: 100%;
			height: 100%;
			display: flex;
			justify-content: center;
			align-items: center;
		}
	}

	.view-more {
		margin-top: 20px;
		background: transparent;
		border: 2px solid $darkblue-color;
		margin: 0 10px;
		padding: 10px 0;
		border-radius: 18px;
		cursor: pointer;
		.arrow {
			font-family: monospace;
			line-height: 10px;
			font-weight: 800;
			margin-left: 10px;
		}
	}

	@media screen and (min-width: 768px) {
		padding: 0 5%;
		.hidden-mobile {
			display: flex;
		}

		.hidden-dekstop {
			display: none;
		}
		.icon-title {
			display: flex;
			justify-content: space-between;
			h2 {
				span {
					font-size: 26px;
					margin-left: 5px;
				}
			}

			.view-more {
				display: flex;
				justify-content: center;
				align-items: center;
				padding: 10px 30px;
				gap: 10px;
			}
		}

		.icon-gallery {
			grid-template-columns: repeat(7, auto);
		}
	}
}
</style>
