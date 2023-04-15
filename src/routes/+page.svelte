<div class="slot" id="slot">
	<div class="slots slot1">
		<div class="slotConatiner c1" />
	</div>
	<div class="slots slot2">
		<div class="slotConatiner c2" />
	</div>
	<div class="slots slot2">
		<div class="slotConatiner c2" />
	</div>
	<div class="slots slot2">
		<div class="slotConatiner c2" />
	</div>
	<div class="slots slot2">
		<div class="slotConatiner c2" />
	</div>
</div>

<style>
	.slot {
		height: 100%;
		overflow: hidden;

		margin-bottom: 5rem;
		margin-top: 7rem;
	}
	.slots {
		height: calc(100vh - 7.2rem);

		width: calc(100% - 20px);
		margin: 0 10px;

		display: flex;
		align-items: start;
		justify-content: center;
		border-bottom: 5px solid var(--optDark);
		background-color: var(--secondary);
	}
	.slotConatiner {
		height: calc(100% - 20px);
		width: calc(100% - 20px);
		margin: 10px;
		background-color: var(--primary);
	}
</style>
