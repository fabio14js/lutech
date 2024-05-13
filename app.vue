<script setup lang="ts">
const route = useRoute();

useHead({
	title: "Lutech | Presentazione Fabio Turi",

	htmlAttrs: {
		lang: "it",
	},

	link: [{ rel: "mask-icon", href: "/safari-pinned-tab.svg", color: "#f5e9f3" }],

	meta: [
		{ charset: "utf-8" },
		{ name: "viewport", content: "width=device-width, initial-scale=1" },
		{ name: "apple-mobile-web-app-title", content: "Lutech presentazione | Fabio Turi" },
		{ name: "application-name", content: "Lutech presentazione | Fabio Turi" },
		{ name: "theme-color", content: "#f5e9f3" },
		{
			name: "description",
			hid: "description",
			content: "Presentazione Lutech Fabio Turi 13/05/2024 | ServiceNow",
		},
	],
});
</script>

<template>
	<NuxtLayout>
		<NuxtPage />
	</NuxtLayout>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&family=Sedan+SC&display=swap");

* {
	font-family: "Roboto", sans-serif;
}

.title-font {
	font-family: "Sedan SC", serif;
}
</style>
