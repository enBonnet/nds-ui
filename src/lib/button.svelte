<script lang="ts">
	import cn from 'classnames';
	export let size: 'sm' | 'md' | 'lg' | 'xl' = 'md';
	export let color: 'green' | 'red' | 'blue' | 'base' = 'base';
	export let disabled: boolean = false;
	export let loading: boolean = false;
	export let href: string | undefined = undefined;
	export let tabindex: number = 0;
  export let external: boolean = false;
	let className: string = '';
	export { className as class };
	const classes = cn('button', className, size, color, { loading, disabled });
</script>

{#if href && !disabled}
	<a {href} {tabindex} role="button" rel="noreferrer noopener" target={external ? '_blank' : '_self'} class={classes} {...$$restProps}>
		<slot />
	</a>
{:else}
	<button on:click {tabindex} {disabled} class={classes} {...$$restProps}>
		<slot />
	</button>
{/if}

<style>
	/* base */
	.button {
		text-decoration: none;
		position: relative;
		font-weight: 700;
		overflow: hidden;
		margin-top: 0.625rem;
		font-size: inherit;
		top: -0.5rem;
		border-radius: 0.625rem;
		color: #050505;
	}
	/* customizations */
	.button.sm {
		padding: 0.5rem 1rem;
	}
	.button.md {
		padding: 0.6875rem 1.375rem;
	}
	.button.lg {
		padding: 0.875rem 1.75rem;
		font-size: 1.375rem;
	}
	.button.xl {
		padding: 1.0625rem 2.125rem;
		font-size: 1.75rem;
	}
	.button.green {
		border: solid 0.125rem #165a38;
		background: #67daa2;
		box-shadow: 0 0.375rem 0 0#165a38;
	}
	.button.green:hover {
		box-shadow: 0 0.25rem 0 0#165a38, 0 0.25rem 0.25rem 0 rgba(0, 0, 0, 0.4);
	}
	.button.green:active {
		top: 0;
		box-shadow: 0 0 0 0#165a38;
	}
	.button.red {
		border: solid 0.125rem #5e1817;
		background: #df7d7c;
		box-shadow: 0 0.375rem 0 0#5e1817;
	}
	.button.red:hover {
		box-shadow: 0 0.25rem 0 0#5e1817, 0 0.25rem 0.25rem 0 rgba(0, 0, 0, 0.4);
	}
	.button.red:active {
		top: 0;
		box-shadow: 0 0 0 0#5e1817;
	}
	.button.blue {
		border: solid 0.125rem #16345a;
		background: #679fda;
		box-shadow: 0 0.375rem 0 0#16345a;
	}
	.button.blue:hover {
		box-shadow: 0 0.25rem 0 0#16345a, 0 0.25rem 0.25rem 0 rgba(0, 0, 0, 0.4);
	}
	.button.blue:active {
		top: 0;
		box-shadow: 0 0 0 0#16345a;
	}
	.button.base {
		border: solid 0.125rem #8d8a86;
		background: #c3c2c0;
		box-shadow: 0 0.375rem 0 0#8d8a86;
	}
	.button.base:hover {
		box-shadow: 0 0.25rem 0 0#8d8a86, 0 0.25rem 0.25rem 0 rgba(0, 0, 0, 0.4);
	}
	.button.base:active {
		top: 0;
		box-shadow: 0 0 0 0#8d8a86;
	}
	/* status */
	.button:hover {
		cursor: pointer;
		top: -0.25rem;
	}
	.button:focus {
		outline: solid 0.25rem #d8b600;
		background: #ffd90c;
		outline-offset: -0.375rem;
		color: #050505;
		text-decoration: none;
		opacity: 1;
	}
</style>
