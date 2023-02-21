<script>
	import '../lib/styles/base.css';
	import Button from '../lib/button.svelte';
</script>

<div>
	Buttons
	<div class="buttons">
		<div class="sm">
			<Button size="sm">Button</Button>
			<Button size="sm" color="green">Button</Button>
			<Button size="sm" color="red">Button</Button>
			<Button size="sm" color="blue">Button</Button>
		</div>
		<div class="md">
			<Button>Button</Button>
			<Button color="green">Button</Button>
			<Button color="red">Button</Button>
			<Button color="blue">Button</Button>
		</div>
		<div class="lg">
			<Button size="lg">Button</Button>
			<Button size="lg" color="green">Button</Button>
			<Button size="lg" color="red">Button</Button>
			<Button size="lg" color="blue">Button</Button>
		</div>
		<div class="xl">
			<Button size="xl">Button</Button>
			<Button size="xl" color="green">Button</Button>
			<Button size="xl" color="red">Button</Button>
			<Button size="xl" color="blue">Button</Button>
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