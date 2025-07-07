<script lang="ts">
	import { BASE_PATH, WEBUI_BASE_URL } from '$lib/constants';

	export let className = 'size-8';
	export let src = `${BASE_PATH}/static/favicon.png`;
</script>

<img
	crossorigin="anonymous"
	src={src === ''
		? `${BASE_PATH}/static/favicon.png`
		: src.startsWith(WEBUI_BASE_URL) ||
			  src.startsWith('https://www.gravatar.com/avatar/') ||
			  src.startsWith('data:') ||
			  src.startsWith('/')
			? src
			: `${BASE_PATH}/user.png`}
	class=" {className} object-cover rounded-full"
	alt="profile"
	draggable="false"
/>
