<script lang="ts">
	import { cn } from '$lib';
	import type { HTMLInputAttributes } from 'svelte/elements';
	let {
		value = $bindable(''),
		class: className,
		...props
	}: HTMLInputAttributes = $props();
</script>

<input
	bind:value
	type="text"
	class={cn(
		'h-10 w-full rounded bg-foreground-80 px-3 text-sm placeholder-main-60 outline-none',
		className,
	)}
	{...props}
/>
