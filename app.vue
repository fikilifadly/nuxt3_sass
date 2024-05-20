<template>
	<!-- <header>not complete</header> -->
	<main>
		<HeroBanner />
		<Cards :pets="pets" :heading="headingDog" :qoute="qouteDog" />
		<BannerCta />
		<Cards :pets="petsGift" :heading="headingGift" :qoute="qouteGift" />
		<IconList :title="titleIcon" :highlight="headingIcon" :icons="icons" />
	</main>
</template>

<script setup>
import HeroBanner from "@/components/HeroBanner.vue";
import "@/assets/css/global.scss";
import Cards from "./src/components/Cards.vue";
import BannerCta from "./src/components/BannerCta.vue";
import IconList from "./src/components/IconList.vue";

// card 1
const headingDog = "Take A Look At Some Of Our Pets";
const qouteDog = "Whats new?";

// card 2
const headingGift = "Our Products";
const qouteGift = "Hard to choose right products for your pets?";

// icon title
const titleIcon = "Proud to be part of ";
const headingIcon = "Pet Sellers";

// icons
const pets = [
	{
		id: 1,
		name: "Pomeranian",
		breed: "Pomeranian",
		gender: "Male",
		age: "3",
		price: "6.200.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 2,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 3,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 4,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 5,
		name: "Pomeranian",
		breed: "Pomeranian",
		gender: "Male",
		age: "3",
		price: "6.200.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 6,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 7,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
	},
	{
		id: 8,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
	},
];

const petsGift = [
	{
		id: 1,
		name: "Pomeranian",
		breed: "Pomeranian",
		gender: "Male",
		age: "3",
		price: "6.200.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 2,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 3,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 4,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 5,
		name: "Pomeranian",
		breed: "Pomeranian",
		gender: "Male",
		age: "3",
		price: "6.200.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 6,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 7,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
	{
		id: 8,
		name: "Poodle Tiny",
		breed: "Poodle Tiny",
		gender: "Male",
		age: "3",
		price: "5.700.000 VND",
		imageUrl: "/dog.webp",
		gift: "Dog Food",
	},
];

const icons = [
	{
		icon: "/seler_1.png",
	},
	{
		icon: "/seler_2.png",
	},
	{
		icon: "/seler_3.png",
	},
	{
		icon: "/seler_4.png",
	},
	{
		icon: "/seler_5.png",
	},
	{
		icon: "/seler_6.png",
	},
	{
		icon: "/seler_7.png",
	},
];
</script>
