<script lang="ts">
	import '$lib/Styles/app.css';
	import Navs from '$lib/components/Navs.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		window.scrollTo(0, 0);
	});

	let lastScrollPosition = 0;
	const handleScroll = () => {
		const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;
		const isScrollingDown = currentScrollPosition > lastScrollPosition;

		const slot = document.getElementById('slot');
		const topNav = document.getElementById('TopNav');
		const bottomNav = document.getElementById('BottomNav');

		if (slot && topNav && bottomNav) {
			const isScrollEnd = currentScrollPosition + window.innerHeight >= slot.offsetHeight;
			if (isScrollingDown && currentScrollPosition > 100 && !isScrollEnd) {
				topNav.style.top = '-6.2rem';
				bottomNav.style.bottom = '-4.2rem';
			} else if (isScrollEnd) {
				topNav.style.top = '-6.2rem';
				bottomNav.style.bottom = '0';
			} else {
				topNav.style.top = '0';
				bottomNav.style.bottom = '0';
			}
		}

		lastScrollPosition = currentScrollPosition;
	};
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
