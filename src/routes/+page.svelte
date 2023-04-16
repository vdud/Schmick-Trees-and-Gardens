<script lang="ts">
	import Img_One from '$lib/Assets/old-website-images/Old-website-asset-No-1.jpg';
	import Img_Two from '$lib/Assets/old-website-images/Old-website-asset-No-2.jpg';
	import Img_Three from '$lib/Assets/old-website-images/Old-website-asset-No-3.jpg';
	import Img_Four from '$lib/Assets/old-website-images/Old-website-asset-No-4.jpg';

	import gradient1 from '$lib/Assets/gradients/1x/Asset 2.png';

	const navShow = () => {
		const bottomNav = document.getElementById('BottomNav');

		if (bottomNav) {
			bottomNav.style.bottom = '0';
		}
	};
</script>

<!-- /Users/varundudeja/Documents/Schmick-Trees-and-Gardens/src/lib/ -->

<div class="slot" id="slot">
	<div class="slots slot1">
		<div class="imgContainer">
			<div class="grad" />
			<img class="imgSlot" src={Img_Two} alt="Gardening, cutting grass" />
		</div>
		<div class="slotConatiner c2">
			<div class="InfoBox">
				<h1>Nature's Finest: Elite Tree, Garden & Mowing Services 🌳 🌺</h1>
				<p>Discover exceptional care for your green spaces in Albany and the Great Southern region. Let our skilled team revitalize your trees, gardens, and lawns!</p>
				<p class="small">✨ Contact our friendly experts now - Elevate your outdoors! ✨</p>
			</div>
			<div class="slotGrad" />
		</div>
	</div>
	<div class="slots slot2">
		<div class="imgContainer">
			<div class="grad" />
			<!-- <img class="imgSlot" src={gradient1} alt="Gardening, cutting grass" /> -->
		</div>
		<div class="slotConatiner c2">
			<div class="InfoBox">
				<h1>Service Zones 📍</h1>
				<p>Schmick Trees & Gardens offers a range of solutions, focusing on 3 core areas.</p>
				<p class="small">Tap the box most relevant to you above and discover how we can assist! 🌳 🌺</p>
			</div>
			<div class="servicesFlex">
				<button on:click={navShow} class="flex flex1">
					<div class="imgContainer scale2">
						<div class="grad" />
						<img class="imgSlotFlex" src={Img_Two} alt="Gardening, cutting grass" />
					</div>
					<div class="FlexInfo">
						<p class="FlexInfoText">Mowing</p>
					</div>
				</button>
				<button on:click={navShow} class="flex flex2">
					<div class="imgContainer scale2">
						<div class="grad" />
						<img class="imgSlotFlex" src={Img_Four} alt="Gardening, cutting grass" />
					</div>
					<div class="FlexInfo">
						<p class="FlexInfoText">Trees</p>
					</div></button>
				<button on:click={navShow} class="flex flex3">
					<div class="imgContainer scale2">
						<div class="grad" />
						<img class="imgSlotFlex" src={Img_One} alt="Gardening, cutting grass" />
					</div>
					<div class="FlexInfo">
						<p class="FlexInfoText">Gardens</p>
					</div></button>
			</div>
			<div class="slotGrad" />
		</div>
	</div>
	<div class="slots slot3">
		<div class="imgContainer">
			<div class="grad" />
			<img class="imgSlot" src={Img_Three} alt="Gardening, cutting grass" />
		</div>
		<div class="slotConatiner c2">
			<div class="InfoBox">
				<h1>Lush Lawns by Schmick Mowing 🌱 ✨</h1>
				<p>Create the garden of your dreams with a pristine lawn! Let our experts handle the details for a flawless green space.</p>
				<ul class="small">
					<li>🌱 Mowing for all lawn sizes</li>
					<li>🚜 Block slashing & clearing</li>
					<li>✂️ Precision whipper snipping</li>
					<li>🌼 Fertilizing for healthy growth 🌿</li>
					<li>📏 Edging & hedging mastery 🌳</li>
					<li>🚫 Weed control & prevention 🌱</li>
					<li>🧽 Garden cleanups & maintenance 🌺</li>
					<li>🪴 Skillful pruning ✂️</li>
					<li>🎉🌸 And so much more... 🌿🌼</li>
				</ul>
			</div>
			<div class="slotGrad" />
		</div>
	</div>
	<div class="slots slot4">
		<div class="imgContainer">
			<div class="grad" />
			<img class="imgSlot" src={Img_Four} alt="Gardening, cutting grass" />
		</div>
		<div class="slotConatiner c2">
			<div class="InfoBox">
				<h1>Schmick Trees: Albany's Arborist All-Stars 🌳 🌟</h1>
				<p>Experience top-tier tree care with our comprehensive, professional services. We've got your tree needs covered from roots to crown!</p>
				<ul class="small">
					<li>🌳 Expert tree removal & felling 🌳</li>
					<li>✂️ Precision tree lopping ✔️</li>
					<li>🔝 Canopy lifting for better views 🌄</li>
					<li>🚧 Safe tree limb removals 🌿</li>
					<li>🚜 Stump removal & grinding 💥</li>
					<li>🌿 Masterful pruning & hedging ✂️</li>
					<li>🍂 Mulching & wood chipping 🔄</li>
					<li>🏛️ Council-approved works ✅</li>
					<li>🧹 Complete yard cleanups 🏡</li>
					<li>🎉 And so much more… 🍃 🌲</li>
				</ul>
			</div>
			<div class="slotGrad" />
		</div>
	</div>
	<div class="slots slot5">
		<div class="imgContainer">
			<div class="grad" />
			<img class="imgSlot" src={Img_One} alt="Gardening, cutting grass" />
		</div>
		<div class="slotConatiner c2">
			<div class="InfoBox">
				<h1>Schmick Gardens: Albany's Landscaping Pros 🌺 🌟</h1>
				<p>Crafting stunning outdoor spaces with our top-notch gardening services. Let us bring your dream garden to life!</p>
				<ul class="small">
					<li>🌿 Landscaping & design</li>
					<li>🧱 Paving mastery</li>
					<li>🚜 Earth moving expertise</li>
					<li>💪 Retaining wall construction</li>
					<li>🌼 Regular garden maintenance</li>
					<li>💦 Reticulation installation & repair</li>
					<li>🍂 Mulching magic</li>
					<li>🌳 Tree lopping & pruning</li>
					<li>🌱 Weeding & mowing</li>
					<li>🌸 Fertilizing for lush lawns & gardens</li>
					<li>🧹 General garden cleanup</li>
					<li>🎉 And so much more... 🌿🌼</li>
				</ul>
			</div>
			<div class="slotGrad" />
		</div>
	</div>
</div>

<style>
	.small {
		font-size: 0.75rem;
		font-weight: 100;
		text-transform: uppercase;
		opacity: 0.75;
	}
	.scale2 {
		scale: 1.2;
	}
	.imgSlotFlex {
		width: 100%;
		z-index: 0;
	}

	.FlexInfoText {
		font-size: 1.2rem;
		font-weight: 600;

		color: var(--primaryTheme);
	}
	.FlexInfo {
		position: absolute;
		bottom: 0;
		left: 0;
		width: 100%;
		/* height: fit-content; */

		background-color: var(--primaryThemeInverted);
		/* contain text */
		white-space: normal;
	}
	.servicesFlex {
		position: absolute;
		top: calc(var(--averageMargin) * 4);
		left: calc(var(--averageMargin) * 2);

		width: calc(100% - var(--averageMargin) * 4);

		height: 45%;

		display: flex;
		align-items: center;
		justify-content: space-evenly;

		overflow: hidden;
	}
	.flex {
		/* margin: 3px; */
		/* width: 33.33%; */
		width: calc(100% / 3 - 6px);
		height: calc(100% - 6px);
		background-color: var(--primaryTheme);
		overflow: hidden;

		border-radius: var(--borderRadius);
		box-shadow: var(--boxShadows);
		border: 1px solid var(--primaryThemeInverted);

		position: relative;
	}
	.imgContainer {
		position: absolute;
		top: 0;
		left: 0;

		height: max-content;
		width: 100%;
		z-index: 0;
	}
	.grad {
		position: absolute;
		height: 100%;
		width: 100%;
		background: linear-gradient(180deg, #0000, var(--primaryTheme));
		z-index: 1;
	}
	.imgSlot {
		width: 100%;
		z-index: 0;
	}
	.slot {
		height: 100%;
		overflow: hidden;

		margin-bottom: 5rem;
		margin-top: 7rem;
	}
	.slots {
		overflow: hidden;

		/* height: calc(100vh - 7.2rem); */
		height: 600px;

		width: calc(100% - 20px);
		margin: 9px;

		display: flex;
		align-items: start;
		justify-content: center;
		background-color: var(--primaryTheme);
		/* background-color: var(--primary); */
		border: 1px solid var(--tertiaryThemeInverted);
		border-radius: var(--borderRadius);
		box-shadow: var(--boxShadows);

		position: relative;
	}
	.slot2 {
		height: 450px;
	}
	.slot5 {
		height: 750px;
	}
	.slotConatiner {
		/* height: calc(100% - 20px); */
		/* width: calc(100% - 20px); */
		/* margin: 10px; */
		height: 100%;
		width: 100%;
		/* z-index: 0; */

		display: flex;
		align-items: end;
		justify-content: center;
	}
	.slotGrad {
		height: 50%;
		width: 100%;
		position: absolute;
		bottom: 0;
		z-index: 1;

		/* background-color: #fff1; */
		background: linear-gradient(180deg, #0000, var(--primaryTheme));
	}
	.InfoBox {
		/* height: fit-content; */
		width: 80%;

		display: flex;
		align-items: start;
		padding: 20px;
		justify-content: end;
		flex-direction: column;
		color: var(--primaryThemeInverted);
		background: linear-gradient(0deg, #0000, var(--tertiaryTheme));

		z-index: 2;

		/* background blur */
		backdrop-filter: blur(3px);
		/* webkit too */
		-webkit-backdrop-filter: blur(3px);

		border-radius: 10px;
		border-top: 1px solid var(--tertiaryThemeInverted);
		margin-bottom: var(--averageMargin);
	}
</style>
