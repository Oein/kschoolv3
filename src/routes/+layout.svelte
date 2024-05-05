<script lang="ts">
	import { afterNavigate } from '$app/navigation';
	import '@/styles/global.css';
	import { onMount } from 'svelte';

	let top: HTMLElement;
	afterNavigate((nav) => {
		if (nav.type === 'link') {
			top?.scrollIntoView();
			console.log('scrolling to top');
		}
	});

	// import {checkSession, user as ustore, type IUser} from './session';
	// onMount(() => {
	// 	if(typeof window == 'undefined') return;
	// 	checkSession();
	// })
	// let user: IUser | null = null;
	// ustore.subscribe((v) => {
	// 	user = v;
	// });
</script>

<div class="App">
	<header>
		<h1 class="appname">
			<a href="/"> K학교전 </a>
		</h1>
		<!-- {#if user == null}
		<a
			class="signin"
			href="https://api.instagram.com/oauth/authorize?client_id=355758490756147&redirect_uri=https://dj.daejeon.kr/auth/callback/&response_type=code&scope=user_profile"
		>
			로그인
		</a>
		{:else}
			<div>@{user.username}</div>
		{/if} -->
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
	<title>대전, 대신 전해드립니다.</title>
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
		/* max-width: 840px; */
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
		/* max-width: 840px; */
		overflow: hidden;
		margin: 0px auto;
	}

	main {
		/* max-width: 840px; */
		/* height: 100dvh; */
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
		/* max-width: 840px; */
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

	.appname > a > img {
		/* width: 64px; */
		height: 1.2em;
		margin-right: 8px;
	}

	.appname {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: start;
		/* width: 100%; */
		flex-grow: 1;
		margin: 0px;
		padding: 0px;
	}

	/* .signin {
		width: fit-content;
		min-width: fit-content;
	} */
</style>
