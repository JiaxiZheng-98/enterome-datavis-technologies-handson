<script>
	let clicked = false;
</script>

<div>
	{#if !clicked}
		<button class="btn btn-primary" on:click={() => (clicked = true)}>
			You have to click the button!
		</button>
	{/if}
	{#if clicked}
		<button class="btn btn-primary" on:click={() => (clicked = true)}>
			You have clicked the button!
		</button>
	{/if}
</div>