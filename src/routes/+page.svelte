<div class="slot" id="slot">
	<div class="slots slot1">
		<div class="slotConatiner c1" />
	</div>
	<div class="slots slot2">
		<div class="slotConatiner c2" />
	</div>
</div>

<style>
	.slot {
		height: 100%;
		overflow: hidden;

		background-color: red;
		margin-bottom: 4.8rem;
	}
	.slots {
		height: 100vh;

		width: calc(100% - 20px);
		margin: 0 10px;

		display: flex;
		align-items: start;
		justify-content: center;
		padding-top: 7rem;

		/* height: calc(100vh - 18rem); */

		/* margin-top: 6rem; */
	}
	.slot1 {
		background-color: yellowgreen;
	}
	.slot2 {
		background-color: blue;
	}
	.slotConatiner {
		/* height: calc(100% - 11.6rem); */
		height: 100%;
		width: calc(100% - 20px);
		margin: 0 10px;
	}
	.c1 {
		background-color: yellow;
	}
	.c2 {
		background-color: hotpink;
	}
</style>
