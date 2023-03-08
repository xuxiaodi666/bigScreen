<template>
	<div class="detle">
		<Echartsolt></Echartsolt>
		<div ref="chartColumn" style="width:100%; height:400px;"></div>
		<img :src="bottomimg" class="imgb">
		<Echartsolt>
			<template slot="slot01">
				趋势分析
			</template>	
		</Echartsolt>
		<!-- 折线图 -->
		<Dataarry></Dataarry>
	</div>
</template>

<script>
	import Echartsolt from "@/components/home/Echartsolt.vue"
	import * as echarts from 'echarts'
	import logo from "@/assets/image/bottomline.png";
	import Dataarry  from "@/components/home/Dataarry.vue"
	export default {
		data() {
			return {
				bottomimg:logo,
				chartColumn: null,
				option: {
					xAxis: [{
						data:['驻地', '驻地', '驻地', '驻地', '驻地', '驻地', '驻地', '驻地'],
						
						axisLabel: {
							
							textStyle: {
								fontSize: '12',
								color: '#fff' // 坐标值的具体的颜色
							},
							// 设置字体的倾斜角度
							interval: 0,
							rotate: 30
						},
						axisLine: {
							lineStyle: {
								color: '#86A5C3', // 轴线的颜色
								line:'dashed'
							}
						},
						splitLine: { // 去除背景网格线
							show: false
						}
					}],
					yAxis: {},
					series: [{
						name: '销量',
						type: 'bar',
						data: [5, 20, 36, 10, 10, 20,0,0],
						showBackground: true,
						backgroundStyle: {
							color: 'rgba(180,180,180,0.2)'
						}
					}]
				},
				data: [5, 20, 36, 10, 10, 20, 5, 20, 36, 10, 20, 36, 10, 10, 20, 5, 20, 36, 10]
			}
		},
		components: {
			Echartsolt,
			Dataarry
		},
		methods: {
			changeOption() {
				var r = Math.floor(Math.random() * 12)
				var d = this.data.slice(r, r + 6)
				this.option.series[0].data = d
				this.chartColumn.setOption(this.option)
			},
			initChart() {
				this.chartColumn = echarts.init(this.$refs.chartColumn)
				this.chartColumn.setOption(this.option)
			}
		},
		mounted() {
			// 柱状图数据渲染
			this.initChart()
		}
	}
</script>

<style scoped>
	.detle {
		width: 100%;
		padding: 15px 10px;
		box-sizing: border-box;
	}
	.imgb{
		height: 20px;
	}
</style>
