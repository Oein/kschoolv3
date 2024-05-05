<script lang="ts">
	import { page } from '$app/stores';
	import Err from './err.svelte';

	let title = $page.url.searchParams.get('title');
	let message = $page.url.searchParams.get('desc') || "";
</script>

<Err title={title == null ? "어라? 무언가가 잘못되었어요" : title} desc={message} />
