<template>
	<div class="quality">
		<!-- <div class="title">
			<span>
				质量整改
			</span>
			<span>
				安全整改
			</span>
		</div> -->
		<div class="title">
			<Tabs v-model="activeKey">
				<Pane label="质量整改" name="1">
					<ul>
						<li v-for="(item,index) in lidata" :key="index">
							{{item.title}}
							<p class="changet">
								{{item.time}}
								<span>{{item.stuts}}</span>
							</p>
							<p class="img"></p>
						</li>
					</ul>
				</Pane>
				<Pane label="安全整改" name="2">
					<ul>
						<li v-for="(item,index) in lidatas" :key="index">
							{{item.title}}
							<p class="changet">
								{{item.time}}
								<span>{{item.stuts}}</span>
							</p>
							<p class="img"  style="background-color: indianred;"></p>
						</li>
					</ul>
				</Pane>
			</Tabs>
		</div>
		
		<p>
			分页
		</p>
	</div>
</template>

<script>
	import Tabs from "@/components/common/tab.vue";
	import Pane from "@/components/common/pane.vue";
	export default {
		data() {
			return {
				lidata: [{
						title: "063",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
					{
						title: "063",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
					{
						title: "063",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
					{
						title: "063",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
				],
				lidatas: [{
						title: "6666666",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
					{
						title: "666666",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
					{
						title: "666666",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
					{
						title: "333333333333",
						time: "2022-12-12 T19:20",
						stuts: "已完成"
					},
				],
				activeKey: '1'
			}
		},
		components: {
			Tabs,
			Pane
		}
	}
</script>

<style scoped>
	.quality {
		margin-top: 15px;
		padding-left: 15px;
		box-sizing: border-box;
	}

	.title {
		width: 100%;
	}

	.title span {
		color: white;
		margin-right: 20px;
	}

	.quality ul {
		width: 100%;
		box-sizing: border-box;
		display: flex;
		justify-content: space-between;
		margin-top: 15px;
		flex-wrap: wrap;
	}

	.quality ul li {
		width: calc(50% - 30px);
		background: white;
		background-color: rgba(255, 255, 255, 0.2);
		display: flex;
		flex-direction: column;
		border-radius: 5px;
		color: white;
		padding: 10px;
		margin-bottom: 10px;
	}

	.changet {
		display: flex;
		justify-content: space-between;
		margin: 15px 0;
	}

	.changet span {
		padding: 5px 10px;
		background-color: #76a561;
		border-radius: 4px;
	}

	.quality ul li .img {
		width: 100%;
		height: 190px;
		background-color: white;
		border-radius: 8px;
	}

	.tabs {
		font-size: 14px;
		color: #657180;
	}

	.tabs-bar:after {
		content: '';
		display: flex;
		justify-content: left;
		width: 100%;
		height: 1px;
		background: #d7dde4;
		margin-top: -1px;
	}

	.tabs-tab {
		display: inline-block;
		padding: 4px 16px;
		margin-right: 6px;
		background: #fff;
		border: 1px solid #d7dde4;
		cursor: pointer;
		position: relative;
	}

	.tabs-content {
		padding: 8px 0;
	}
</style>
