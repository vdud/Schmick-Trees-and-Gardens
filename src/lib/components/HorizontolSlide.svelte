<script lang="ts">
	import Img_One from '$lib/Assets/old-website-images/Old-website-asset-No-1.jpg';
	import Img_Two from '$lib/Assets/old-website-images/Old-website-asset-No-2.jpg';
	import Img_Four from '$lib/Assets/old-website-images/Old-website-asset-No-4.jpg';

	const navShow = () => {
		const bottomNav = document.getElementById('BottomNav');

		if (bottomNav) {
			bottomNav.style.bottom = '0';
		}
	};
</script>

<div class="Slot">
	<div class="flexBoxy">
		<button on:click={navShow} class="box box1">
			<div class="ImgCont">
				<div class="gradFlex" />
				<img class="imgFlex" src={Img_One} alt="Gardening, cutting grass" />
				<p class="flexText">Gardens</p>
			</div>
		</button>
		<button on:click={navShow} class="box box2">
			<div class="ImgCont">
				<div class="gradFlex" />
				<img class="imgFlex" src={Img_Two} alt="Gardening, cutting grass" />
				<p class="flexText">Trees</p>
			</div>
		</button>
		<button on:click={navShow} class="box box3">
			<div class="ImgCont">
				<div class="gradFlex" />
				<img class="imgFlex" src={Img_Four} alt="Gardening, cutting grass" />
				<p class="flexText">Trees</p>
			</div>
		</button>
	</div>
	<div class="textBox">
		<div class="InfoBox">
			<h1>Service Zones 📍</h1>
			<p>Schmick Trees & Gardens offers a range of solutions, focusing on 3 core areas.</p>
			<p class="small">Tap the box most relevant to you above and discover how we can assist! 🌳 🌺</p>
		</div>
	</div>
</div>

<style>
	.flexText {
		position: absolute;
		color: var(--primaryThemeInverted);
		background-color: red;
		padding: 3px 10px;
		padding-top: 25px;

		font-size: 2rem;
	}
	.gradFlex {
		width: 100%;
		height: 100%;
		background-image: linear-gradient(#0000, green);

		position: absolute;
	}
	.ImgCont {
		height: 100%;
		width: 100%;
		overflow: hidden;

		display: flex;
		align-items: center;
		justify-content: center;

		position: relative;
	}
	.imgFlex {
		height: 100%;
		width: 100%;
		object-fit: cover;
	}
	.textBox {
		height: 30%;
		width: 100%;
		background-color: green;

		display: flex;
		align-items: center;
		justify-content: center;
		/* overflow: hidden; */
	}
	.Slot {
		height: 100%;
		width: 100%;
		overflow: hidden;
		background-color: red;
	}
	.flexBoxy {
		display: flex;
		/* flex-direction: column; */
		align-items: start;
		justify-content: start;

		height: 70%;
		width: 100%;
		overflow: hidden;
		background-color: blue;
	}
	.box {
		height: 100%;
		width: 100%;

		overflow: hidden;
		transition: filter 0.5s ease-in-out;
	}
	.box:hover {
		filter: brightness(0.8);
	}
	.box1 {
		background-color: yellow;
	}
	.box2 {
		background-color: forestgreen;
	}
	.box3 {
		background-color: antiquewhite;
	}
</style>
