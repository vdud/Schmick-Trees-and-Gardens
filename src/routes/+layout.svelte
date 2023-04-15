<script lang="ts">
	import '$lib/Styles/app.css';

	import TopNav from '$lib/components/TopNav.svelte';
	import { debounce } from '$lib/functions/debounce';
	import BottomNav from '$lib/components/BottomNav.svelte';

	let lastScrollPosition = 0;
	const handleScroll = () => {
		console.log('handle');
		const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;
		const isScrollingDown = currentScrollPosition > lastScrollPosition;
		console.log('currentScrollPosition', currentScrollPosition);

		const slot = document.getElementById('slot');
		const topNav = document.getElementById('TopNav');
		const bottomNav = document.getElementById('BottomNav');

		if (slot && topNav && bottomNav) {
			if (isScrollingDown && currentScrollPosition > 10) {
				topNav.style.top = '-6rem';
				bottomNav.style.bottom = '-3rem';
			} else {
				topNav.style.top = '0';
				bottomNav.style.bottom = '0';
			}
		}

		lastScrollPosition = currentScrollPosition;
	};

	const debouncedHandleFunction = debounce(handleScroll, 33);
</script>

<div class="body">
	<TopNav />
	<slot />
	<BottomNav />
</div>

<svelte:window on:scroll={debouncedHandleFunction} />

<style>
	.body {
		height: 100%;
		width: 100%;

		background-color: white;

		overflow: hidden;
	}
	main {
	}
</style>
