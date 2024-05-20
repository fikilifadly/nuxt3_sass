<template>
	<div class="banner-cta">
		<div class="banner-wrapper">
			<NuxtImg
				src="/Banner_Desktop.webp"
				alt="banner-image"
				loading="lazy"
				class="banner-img"
				srcset="
      /Banner_Desktop.webp 640w,
      /Banner_Card.webp 1024w
    "
				sizes="(min-width: 1024px) 100vw, 640px"
			/>
			<div class="banner-description">
				<h2>One More Friend</h2>
				<h3>Thousands More Fun!</h3>
				<p>Having a pet means you have more joy, a new friend, a happy person who will always be with you to have fun. We have 200+ different pets that can meet your needs!</p>
				<div class="cta-button">
					<button class="cta-primary">View Intro <img src="../assets/icons/Play_Circle.png" alt="btn-play" loading="lazy" class="icon" /></button>
					<button class="cta-secondary">Explore Now</button>
				</div>
			</div>
		</div>
	</div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../assets/css/variables.scss";

.banner-cta {
	height: 640px;
	width: 100%;
	padding: 0 2.5%;

	.banner-wrapper {
		border-radius: 20px;
		height: auto;
		overflow: hidden;
		padding: 0 5px;
		position: relative;

		.banner-img {
			width: 100%;
			height: 100%;
			object-fit: cover;
		}

		.banner-description {
			position: absolute;
			top: 25px;
			left: 7.5%;
			display: flex;
			flex-direction: column;
			gap: 10px;
			justify-content: center;
			align-items: center;
			width: 90%;

			h2 {
				font-size: 28px;
				color: $darkblue-color;
				font-weight: 800;
			}

			h3 {
				font-size: 22px;
				color: $darkblue-color;
				font-weight: 600;
			}

			p {
				font-size: 12px;
				text-align: center;
				line-height: 18px;
			}

			.cta-button {
				display: flex;
				flex-wrap: wrap;
				gap: 15px;
				button {
					border-radius: 50px;
					font-size: 16px;
					height: 48px;
					padding: 0 28px;
					margin-top: 20px;
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
					cursor: pointer;
				}

				.cta-secondary {
					background-color: $darkblue-color;
					color: white;
					border: unset;
					cursor: pointer;
				}
			}
		}
	}

	@media screen and (min-width: 768px) {
		padding: 0 5%;
		height: auto;

		.banner-wrapper {
			.banner-img {
				border-radius: 30px;
			}

			.banner-description {
				top: 50px;
				left: unset;
				right: 50px;
				width: 100%;
				justify-content: end;
				align-items: end;
				text-align: right;
				gap: unset;

				h2 {
					font-size: 58px;
				}

				h3 {
					font-size: 42px;
				}

				p {
					width: 30%;
					text-align: right;
					margin: 20px 0;
				}

				.cta-button {
					button {
						margin-top: 10px;
						height: 48px;
						padding: 0 28px;
						font-size: 14px;
					}

					.cta-primary {
						gap: 10px;
					}
				}
			}
		}
	}
}
</style>
