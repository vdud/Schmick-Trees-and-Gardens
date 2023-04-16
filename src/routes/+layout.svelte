<script lang="ts">
	import '$lib/Styles/app.css';
	import Navs from '$lib/components/Navs.svelte';
	import { onMount } from 'svelte';

	let topNav: any;
	let bottomNav: any;
	let slot: any;

	onMount(() => {
		window.scrollTo(0, 0);
		topNav = document.getElementById('TopNav');
		bottomNav = document.getElementById('BottomNav');
		slot = document.getElementById('slot');

		bottomNav.style.bottom = '-4.2rem';
	});

	let lastScrollPosition = 0;

	const handleScroll = () => {
		const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;
		const isScrollingDown = currentScrollPosition > lastScrollPosition;
		const isScrollingUp = currentScrollPosition < lastScrollPosition;

		// const isScrollEnd = currentScrollPosition + window.innerHeight >= slot.offsetHeight;
		const isScrollStart = currentScrollPosition < 100;
		// const isScrollStart = currentScrollPosition === 0;

		if (isScrollingDown && !isScrollStart && !isScrollingUp) {
			topNav.style.top = '-6.2rem';
			// bottomNav.style.bottom = '-4.2rem';s
			bottomNav.style.bottom = '0';
		} else if (isScrollStart) {
			topNav.style.top = '0';
			bottomNav.style.bottom = '-4.2rem';
		} else if (isScrollingUp) {
			topNav.style.top = '0';
			bottomNav.style.bottom = '-4.2rem';
		}
		lastScrollPosition = currentScrollPosition;
	};

	// const handleScroll = () => {
	// 	const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;
	// 	const isScrollingDown = currentScrollPosition > lastScrollPosition;

	// 	const isScrollEnd = currentScrollPosition + window.innerHeight >= slot.offsetHeight;
	// 	const isScrollStart = currentScrollPosition === 0;

	// 	// if (isScrollingDown && currentScrollPosition > 100 && !isScrollEnd) {
	// 	if (isScrollingDown && !isScrollEnd && !isScrollStart) {
	// 		topNav.style.top = '-6.2rem';
	// 		// bottomNav.style.bottom = '-4.2rem';
	// 		bottomNav.style.bottom = '0';
	// 	} else if (isScrollEnd) {
	// 		topNav.style.top = '-6.2rem';
	// 		bottomNav.style.bottom = '0';
	// 	} else if (isScrollStart) {
	// 		topNav.style.top = '0';
	// 		bottomNav.style.bottom = '-4.2rem';
	// 	} else {
	// 		topNav.style.top = '0';
	// 		bottomNav.style.bottom = '0';
	// 	}

	// 	lastScrollPosition = currentScrollPosition;
	// };
</script>

<div class="body">
	<Navs />
	<slot />
</div>

<svelte:window on:scroll={handleScroll} />

<style>
	.body {
		height: 100%;
		width: 100%;

		overflow: hidden;
	}
</style>
