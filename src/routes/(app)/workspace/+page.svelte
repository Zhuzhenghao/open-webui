<script lang="ts">
	import { goto } from '$app/navigation';
	import { BASE_PATH } from '$lib/constants';
	import { user } from '$lib/stores';
	import { onMount } from 'svelte';

	onMount(() => {
		if ($user?.role !== 'admin') {
			if ($user?.permissions?.workspace?.models) {
				goto(`${BASE_PATH}/workspace/models`);
			} else if ($user?.permissions?.workspace?.knowledge) {
				goto(`${BASE_PATH}/workspace/knowledge`);
			} else if ($user?.permissions?.workspace?.prompts) {
				goto(`${BASE_PATH}/workspace/prompts`);
			} else if ($user?.permissions?.workspace?.tools) {
				goto(`${BASE_PATH}/workspace/tools`);
			} else {
				goto(`${BASE_PATH}/`);
			}
		} else {
			goto(`${BASE_PATH}/workspace/models`);
		}
	});
</script>
