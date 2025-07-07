<script>
	import { goto } from '$app/navigation';
  import { BASE_PATH } from '$lib/constants';
	import { onMount } from 'svelte';

	import Users from '$lib/components/admin/Users.svelte';

	onMount(() => {
		goto(`${BASE_PATH}/admin/users/overview`);
	});
</script>

<Users />
