<script lang="ts">
	import logoImg from '$lib/Assets/old-website-images/Logo Trans-Shadows.png';
	import BGImg from '$lib/Assets/old-website-images/Old-website-asset-No-6.jpg';

	const navShow = () => {
		const topNav = document.getElementById('TopNav');
		const bottomNav = document.getElementById('BottomNav');
		const slot = document.getElementById('slot');
		const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop;

		if (topNav && bottomNav && slot) {
			if (currentScrollPosition > 100 && topNav.style.top !== '-6.2rem') {
				topNav.style.top = '-6.2rem';
				bottomNav.style.bottom = '-4.2rem';
			} else {
				if (currentScrollPosition === 0 && bottomNav.style.bottom !== '-4.2rem') {
					bottomNav.style.bottom = '-4.2rem';
					topNav.style.top = '0';
				} else {
					topNav.style.top = '0';
					bottomNav.style.bottom = '0';
				}
			}
		}
	};
</script>

<div id="TopNav" class="Nav topNav">
	<div class="NavComponents flexDirectionColumn">
		<div class="component componentCol component1">
			<img class="logoImg" src={logoImg} alt="Schmick Trees & Gardens Mowning" />
			<img class="logoBGImg" src={BGImg} alt="Schmick Trees & Gardens Mowning" />
		</div>
	</div>
</div>

<div id="BottomNav" class="Nav BottomNav">
	<div class="NavComponents flexDirectionRow">
		<button on:click={navShow} class="ContactUs">Contact Us </button>
		<button class="component componentRow component1" />
		<button class="component componentRow component2" />
		<button class="component componentRow component3" />
	</div>
</div>

<style>
	.logoImg {
		height: 100%;
		object-fit: contain;
	}
	.logoBGImg {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		object-fit: contain;
		z-index: -1;
		scale: 1.1;
		filter: blur(2px);
	}
	.ContactUs {
		position: absolute;
		top: 0;
		right: 0;
		width: fit-content;
		height: 1rem;
		background-color: var(--secondary);
		box-shadow: var(--boxShadows);
		color: black;
		z-index: 100;

		display: flex;
		align-items: center;
		justify-content: center;
		overflow: hidden;

		padding: 12px 20px;
		border-radius: var(--borderRadius);

		transform: translate(0%, -85%);
	}
	.Nav {
		position: fixed;
		left: 0;
		box-shadow: var(--boxShadows);
		z-index: 100;

		border-radius: var(--borderRadius);

		width: calc(100% - 60px);
		margin: 9px 29px;
		border: 1px solid var(--tertiaryThemeInverted);

		display: flex;
		align-items: center;
		justify-content: center;
	}
	.topNav {
		top: 0;
		height: 6rem;
		overflow: hidden;

		transition: top 0.3s ease-in-out;
	}
	.BottomNav {
		bottom: 0;
		height: 4rem;

		background-color: var(--primary);
		transition: bottom 0.3s ease-in-out;
	}

	.NavComponents {
		height: 100%;
		width: clamp(100px, 100%, 600px);

		flex-direction: row;
	}
	.flexDirectionRow {
		display: flex;
		justify-content: space-evenly;
		align-items: end;
		margin-bottom: 20px;
		position: relative;
	}
	.flexDirectionColumn {
		/* flex-direction: column; */
	}

	.component {
		border-radius: 6px;
	}

	.componentRow {
		/* height: 6rem; */
		height: calc(100% - 20px);
		width: calc(33% - 10px);

		transition: all 0.3s ease-in-out;

		color: var(--primaryTheme);
		background-color: var(--tertiaryThemeInverted);

		box-shadow: var(--boxShadows);
	}
	.componentRow:hover {
		background-color: var(--secondaryTheme);
		color: var(--primaryThemeInverted);
		box-shadow: var(--boxShadowsBlur);
	}
	.componentRow:active {
		background-color: var(--primaryThemeInverted);
		box-shadow: var(--boxInsetShadows);
	}

	.componentCol {
		height: calc(100% - 20px);
		width: calc(100% - 20px);

		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);

		display: flex;
		align-items: center;
		justify-content: center;
	}
	/* .component1 {
		background-color: blue;
	} */
	/* .component2 {
    background-color: green;
  } */
	/* .component3 {
    background-color: hotpink;
  } */
</style>
