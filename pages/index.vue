<script setup lang="ts">
useHead({
	title: "Lutech | Presentazione Fabio Turi",
});
definePageMeta({
	layout: "default-layout",
});

const currentSlide = ref(0);
</script>

<template>
	<Swiper
		:modules="[SwiperAutoplay, SwiperEffectCreative]"
		:slides-per-view="1"
		:loop="true"
		:effect="'creative'"
		:creative-effect="{
			prev: {
				shadow: false,
				translate: ['-20%', 0, -1],
			},
			next: {
				translate: ['100%', 0, 0],
			},
		}">
		<SwiperSlide @mouseover.prevent="currentSlide = 0">
			<IndexAboutMe />
		</SwiperSlide>
		<SwiperSlide @mouseover.prevent="currentSlide = 1">
			<IndexWeaknesses />
		</SwiperSlide>
		<SwiperSlide @mouseover.prevent="currentSlide = 2">
			<IndexStrengths />
		</SwiperSlide>
	</Swiper>
	<div class="absolute flex gap-3 items-center z-20 bottom-16 left-[50%] translate-x-[-50%]">
		<div
			:class="currentSlide === 0 ? 'bg-slate-600 scale-105' : 'bg-slate-400'"
			class="transition-all duration-200 rounded-full drop-shadow-lg h-3 w-3"></div>
		<div
			:class="currentSlide === 1 ? 'bg-slate-600 scale-105' : 'bg-slate-400'"
			class="transition-all duration-200 rounded-full drop-shadow-lg h-3 w-3"></div>
		<div
			:class="currentSlide === 2 ? 'bg-slate-600 scale-105' : 'bg-slate-400'"
			class="transition-all duration-200 rounded-full drop-shadow-lg h-3 w-3"></div>
		<div
			:class="currentSlide === 3 ? 'bg-slate-600 scale-105' : 'bg-slate-400'"
			class="transition-all duration-200 rounded-full drop-shadow-lg h-3 w-3"></div>
	</div>
</template>
