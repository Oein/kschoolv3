<script>
	import Ulli from './ulli.svelte';
</script>

<h1>이용시 규칙은 무엇이 있나요?</h1>
<p>그러게요 아직 미정인데</p>
<div class="written">
	<p>
		이 내용은 <span class="block">2024년 4월 18일</span>에 업데이트 되어 고지 후 1주일 뒤인
		<span class="block">2024년 4월 25일</span>부터 실행되는 내용입니다.
	</p>
	추후에 변경 사항이 있을수 있음을 고지합니다.
</div>

<style>
	.written {
		text-align: end;
		font-weight: bold;
		margin: 2em 0px;
	}
	.written > p {
		margin: 0px;
	}
	.block {
		padding: 4px 8px;
		border-radius: 4px;
		background: #f5f5f5;
	}

	details {
		background: #f5f5f5;
		border-radius: 8px;
		padding: 8px;
		box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.1);
		margin: 1em 0px;
	}

	summary {
		cursor: pointer;
		user-select: none;
	}
</style>
