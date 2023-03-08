<template>
	<div class="topmenu">
		<span class="goback">返回管理平台</span>
		<div class="btnbox">
			<div>
				<button>工地建档</button>
				<button>工地资讯</button>
				<button>BIM中心</button>
				<button>智能监控</button>
				<button>航拍视频</button>
			</div>
			<div>
				<button>工地建档</button>
				<button>工地资讯</button>
				<button>BIM中心</button>
				<button>智能监控</button>
				<select name="name" placeholder="智能监控">
					<option value="1">智能监控</option>
					<option value="2">智能监控</option>
				</select>
			</div>
		</div>
	</div>
</template>

<script>
</script>

<style scoped>
	.topmenu{
		width: 100%;
		/* height: 20px; */
		background: url("~@/assets/image/topbg.png") no-repeat;
		background-size: 100% auto;
	}
	.goback{
		margin-left: 15px;
		color: #619fcf;
	}
	.btnbox{
		display: flex;
		justify-content: space-between;
		padding: 0 15px;
		box-sizing: border-box;
	}
	.btnbox div{
		width:37%;
		display: flex;
		justify-content: space-between;
		margin-top: 10px;
		
	}
	.btnbox button,.btnbox select{
		border-radius: 50px;
		background: none;
		color: #619fcf;
		border: 1px solid #619fcf;
		padding: 5px 15px;
	}
</style>