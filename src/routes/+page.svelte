<script>
	import Content from './tos/content.svelte';
</script>

<div class="pls">
	<svg class="hd" xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 -960 960 960" width="24"
		><path
			d="M680-39q-17 0-28.5-12T640-80q0-17 11.5-28.5T680-120q66 0 113-47t47-113q0-17 12-29t29-12q17 0 28.5 12t11.5 29q0 100-70.5 170.5T680-39ZM80-640q-17 0-29-11.5T39-680q0-100 70.5-170.5T280-921q17 0 29 11.5t12 28.5q0 17-12 29t-29 12q-66 0-113 47t-47 113q0 17-11.5 28.5T80-640Zm689-143q12 12 12 28t-12 28L515-472q-11 12-27.5 11.5T459-472q-12-12-12-28.5t12-28.5l254-254q12-12 28-12t28 12Zm71 127q12 12 12 28.5T840-599L614-373q-11 11-27.5 11T558-373q-12-12-12.5-28.5T557-430l226-226q12-12 28.5-12t28.5 12ZM211-211q-91-91-91-219t91-219l92-92q12-12 28-12t28 12l31 31q7 7 12 14.5t10 15.5l148-149q12-12 28.5-12t28.5 12q12 12 12 28.5T617-772L444-599l-85 84 19 19q46 46 44 110t-49 111l-1 1q-11 11-27.5 11T316-274q-12-12-12-28.5t12-28.5q23-23 25.5-54.5T321-440l-47-46q-12-12-12-28.5t12-28.5l57-56q12-12 12-28.5T331-656l-64 64q-68 68-68 162.5T267-267q68 68 163 68t163-68l239-240q12-12 28.5-12t28.5 12q12 12 12 28.5T889-450L649-211q-91 91-219 91t-219-91Zm219-219Z"
		/></svg
	>
	<div class="up">안녕하세요!</div>
	<div class="desc">@oein0219와 @inter129가 운영할 예정인 K학교전! (v3) 입니다.</div>
	<div class="sd">
		<svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 -960 960 960" width="24"
			><path
				d="M480-362q-8 0-15-2.5t-13-8.5L268-557q-11-11-11-28t11-28q11-11 28-11t28 11l156 156 156-156q11-11 28-11t28 11q11 11 11 28t-11 28L508-373q-6 6-13 8.5t-15 2.5Z"
			/></svg
		>
		<span>아래로 스크롤하여 더 많은 정보를 확인하세요.</span>
	</div>
</div>
<div class="inf">
	<h1>K학교전이 무엇인가요?</h1>
	<p>팝캣 형식의, 학교 간 클릭 수를 두고 경쟁하는 게임입니다!</p>
	<h1>서비스 오픈은 언제인가요?</h1>
	<p>아직 정확한 오픈 날짜는 정해지지 않았어요. 추후에 공지될 예정이니 궁금하시다면 주기적으로 확인해 주세요!</p>
	<Content />
</div>

<style>
	.inf {
		min-height: calc(100dvh - 128px);
		background: #fff;
		border-top: 1px solid rgba(0, 0, 0, 0.1);
		box-sizing: border-box;
		padding: 8px 1em;
	}
	.inf > h1 {
		margin: 0px;
		margin-top: 1.5em;
	}
	.inf > h1:first-child {
		margin-top: 0px;
	}
	.sd {
		position: absolute;
		left: 50%;
		bottom: 1em;
		transform: translateX(-50%);
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		font-size: 0.85em;
	}
	.pls {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;

		height: calc(100dvh - 64px);
		width: 100%;
		box-sizing: border-box;

		position: relative;
	}
	.hd {
		width: 64px;
		height: 64px;
		font-size: 64px;
		margin-bottom: 0.3em;
	}
	.up {
		font-size: 1.3em;
		font-weight: 600;
		margin-bottom: 4px;
	}
	.desc {
		font-size: 0.9em;
		color: #555;
	}
</style>
