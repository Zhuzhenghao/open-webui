<script>
	import { goto } from '$app/navigation';
  import { BASE_PATH } from '$lib/constants';
	import { onMount } from 'svelte';

	import Evaluations from '$lib/components/admin/Evaluations.svelte';

	onMount(() => {
		goto(`${BASE_PATH}/admin/evaluations/leaderboard`);
	});
</script>

<Evaluations />
