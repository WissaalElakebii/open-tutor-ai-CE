<script>
	import { goto } from '$app/navigation';
	import { onMount } from 'svelte';
	import { browser } from '$app/environment';

	onMount(() => {
		if (!browser) return;
		goto('/parent/dashboard', { replaceState: true });
	});
</script>

<div style="display:flex;align-items:center;justify-content:center;min-height:100vh;background:#F3F4F6;">
	<div style="width:40px;height:40px;border:3px solid #2563EB;border-top-color:transparent;border-radius:50%;animation:spin 1s linear infinite;"></div>
</div>
<style>@keyframes spin { to { transform: rotate(360deg); } }</style>