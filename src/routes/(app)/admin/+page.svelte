<script lang="ts">
	import { goto } from '$app/navigation';
  import { BASE_PATH } from '$lib/constants';
	import { onMount } from 'svelte';

	onMount(() => {
		goto(`${BASE_PATH}/admin/users`);
	});
</script>
