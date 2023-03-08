<template>
	<div class="title">
		<div class="titlecon">
			<slot name='slot01'>
				类型分析
			</slot>
		</div>
	</div>
</template>

<script>
</script>

<style scoped>
	/* .type{
		width: 100%;
		padding:15px 10px;
		box-sizing: border-box;
	} */
	.title {
		width: 100%;
		background: url("~@/assets/image/lined.png");
		background-size: 100% 100%;
		color: white;
		padding-top: 20px;
		padding-left: 10px;
	}

	.title .titlecon {
		width: 80%;
		background: url("~@/assets/image/wei3.png");
		background-size: 100% 100%;
		padding-left: 10px;
		box-sizing: border-box;
	}
</style>
