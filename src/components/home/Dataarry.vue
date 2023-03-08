<template>
	<div class="dataarry">
		<div id="main" style="width: 600px; height:400px;"></div>
	</div>
</template>


<script>
	import * as echarts from 'echarts'
	export default {
		name: "",
		data() {
			return {
				charts: "",
				opinionData: ["3", "2", "4", "4", "5", "3", "2", "4", "4", "5", "4", "5"],
			};
		},
		methods: {
			drawLine(id) {
				this.charts = echarts.init(document.getElementById(id));
				this.charts.setOption({
					grid: {
						top: '20%',
						left: '10%',
						right: '10%',
						bottom: '5%',
						containLabel: true,
					},
					
					xAxis: {
						type: "category",
						boundaryGap: false,
						data: ["1月", "2", "3", "4", "5", "6", "1月", "2", "3", "4", "5", "6"],
					},
					yAxis: {
						type: "value",
						boundaryGap: true,
						background:"#fff",
					},

					series: [{
						type: "line",
						data: this.opinionData,

					}, ],
				});
			},
		},
		//调用
		mounted() {
			this.$nextTick(function() {
				this.drawLine("main");
			});
		},
	};
</script>

<style>
</style>
