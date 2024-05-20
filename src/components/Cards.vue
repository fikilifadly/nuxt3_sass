<template>
	<div class="wrapper">
		<div class="pet-description">
			<span>{{ qoute }}</span>
			<div class="heading-wrapper">
				<h2>{{ heading }}</h2>
				<button class="hidden-mobile view-more">
					<span>View More</span>
					<span class="arrow">></span>
				</button>
			</div>
		</div>
		<div class="pet-gallery">
			<div v-for="pet in pets" :key="pet.id" class="pet-card">
				<div class="img-wrapper">
					<NuxtImg :src="pet.imageUrl" :alt="pet.name" class="pet-image" loading="lazy" />
				</div>
				<div class="pet-details">
					<h3 class="pet-name">{{ pet.name }}</h3>
					<div class="pet-info">
						<p>
							Gene: <span>{{ pet.breed }}</span>
						</p>
						<p>
							Age: <span>{{ pet.breed }}</span>
						</p>
					</div>
					<p class="pet-price">{{ pet.price }}</p>
				</div>
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
const { qoute, heading, pets } = defineProps(["qoute", "heading", "pets"]);
</script>

<style lang="scss" scoped>
@import "../assets/css/variables.scss";

.wrapper {
	display: flex;
	flex-direction: column;
	padding: 0 2.5%;
	margin: 35px 0;
	background-color: $white-color;

	.pet-description {
		display: flex;
		flex-direction: column;
		gap: 7.5px;
		justify-content: center;
		padding: 0 16px;
		margin-bottom: 12.5px;

		span {
			color: $black-color;
			line-height: 20px;
		}

		h2 {
			color: $darkblue-color;
			font-size: 20px;
			line-height: 32px;
		}
	}
	.hidden-mobile {
		display: none;
	}

	.pet-gallery {
		display: grid;
		grid-template-columns: 1fr 1fr;
		justify-content: center;

		.pet-card {
			display: flex;
			flex-direction: column;
			margin: 10px;
			padding: 10px;
			background-color: rgba(253, 253, 253, 1);
			border-radius: 4px;
			box-shadow: 0px 4px 28px -2px rgba(0, 0, 0, 0.08);

			.img-wrapper {
				width: 100%;
				height: 100%;
				border-radius: 15px;
				overflow: hidden;
				margin-bottom: 5px;
			}

			.pet-image {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}

			.pet-details {
				display: flex;
				flex-direction: column;
				gap: 2px;
				margin-top: 10px;
				color: $black-color;

				.pet-name {
					font-size: 14px;
					font-weight: bold;
					line-height: 20px;
				}

				.pet-info {
					color: #666666;
					font-size: 12px;
					margin-bottom: 5px;
					line-height: 18px;
					span {
						font-weight: 700;
					}
				}

				.pet-price {
					color: $black-color;
					font-size: 16px;
					font-weight: 700;
					line-height: 24px;
					margin-bottom: 10px;
				}
			}
		}
	}
	.view-more {
		background: transparent;
		border: 2px solid $darkblue-color;
		margin: 0 10px;
		padding: 10px 0;
		border-radius: 18px;

		.arrow {
			font-family: monospace;
			line-height: 10px;
			font-weight: 800;
		}
	}

	@media screen and (min-width: 768px) {
		padding: 0 5%;

		.hidden-desktop {
			display: none;
		}

		.pet-description {
			.heading-wrapper {
				display: flex;
				justify-content: space-between;
			}
		}
		.hidden-mobile {
			display: flex;
			justify-content: center;
			align-items: center;
			padding: 10px 30px;
			gap: 10px;
		}
		.pet-gallery {
			grid-template-columns: 1fr 1fr 1fr 1fr;

			.pet-card {
				border-radius: 12px;

				.pet-details {
					.pet-info {
						display: flex;
						gap: 25px;

						p {
							position: relative;

							&:nth-child(1)::before {
								content: "";
								position: absolute;
								background-color: #666666;
								border-radius: 100%;
								top: 35%;
								left: 110%;
								width: 4px;
								height: 4px;
							}
						}
					}
				}
			}
		}
	}
}
</style>
