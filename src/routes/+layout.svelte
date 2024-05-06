<script lang="ts">
	import { afterNavigate } from '$app/navigation';
	import '@/styles/global.css';

	let top: HTMLElement;
	afterNavigate((nav) => {
		if (nav.type === 'link') {
			top?.scrollIntoView();
			console.log('scrolling to top');
		}
	});
</script>

<div class="App">
	<header>
		<h1 class="appname">
			<a href="/"> K학교전 </a>
		</h1>
	</header>
	<main>
		<div bind:this={top} />
		<slot />
		<footer>
			<a href="/tos">서비스 약관</a>
			<a href="/privacy">개인정보 처리방침</a>
		</footer>
	</main>
</div>

<svelte:head>
	<title>K학교전</title>
</svelte:head>

<style>
	footer {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		background: white;
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
		z-index: 4;
		width: 100%;
		height: 64px;
		min-height: 64px;
		box-sizing: border-box;
		user-select: none;
		gap: 2em;
	}
	.App {
		display: flex;
		width: 100dvw;
		height: 100dvh;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		overflow: hidden;
		margin: 0px auto;
	}

	main {
		width: 100%;
		flex-grow: 1;
		background: #fff;
		overflow-y: auto;
	}

	header {
		display: flex;
		flex-direction: row;
		align-items: center;
		padding: 0.5em 1em;
		justify-content: start;
		border-bottom: 1px solid rgba(0, 0, 0, 0.1);
		background: white;
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
		z-index: 4;
		width: 100%;
		height: 64px;
		min-height: 64px;
		box-sizing: border-box;
		user-select: none;
	}

	.appname > a {
		line-height: 1;
		display: block;
		height: fit-content;
		display: flex;
		align-items: center;
	}


	.appname {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: start;
		flex-grow: 1;
		margin: 0px;
		padding: 0px;
	}

</style>
