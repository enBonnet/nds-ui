<script>
	import '../lib/styles/base.css';
	import Button from '../lib/button.svelte';
</script>

<div>
	Buttons
	<div class="buttons">
		<div class="md">
			<Button>Button</Button>
			<Button color="green">Button</Button>
			<Button color="red">Button</Button>
			<Button color="blue">Button</Button>
		</div>
	</div>
</div>

<style>
	.buttons > div {
		display: flex;
		gap: 16px;
	}
	.buttons > div:not(:last-child) {
		margin-bottom: 10px;
	}
</style>