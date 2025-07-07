<script>
	import { goto } from '$app/navigation';
  import { BASE_PATH } from '$lib/constants';
	import { onMount } from 'svelte';
	import Settings from '$lib/components/admin/Settings.svelte';

	onMount(() => {
		goto(`${BASE_PATH}/admin/settings/general`);
	});
</script>

<Settings />
