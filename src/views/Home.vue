<template>
	<div class="home">
		<Topmenu></Topmenu>
		<div class="maincon">
			<div class="con">
				<Quality></Quality>
			</div>
			<div class="con">
				<Type></Type>
			</div>
		</div>
	</div>
</template>

<script>
	import Topmenu from'@/components/home/Topmenu.vue'
	import Quality from'@/components/home/Quality.vue'
	import Type from'@/components/home/Type.vue'
	export default {
		name: 'Home',
		components: {
			Topmenu,
			Quality,
			Type
		}
	}
</script>
<style scoped>
	.home {
		width: 100%;
		height: 100%;
		background: url("~@/assets/image/bg.png");
		background-size: 100% 100%;
		position: fixed;
		overflow-y: scroll;
	}
	.maincon{
		width: 100%;
		display: flex;
		justify-content: space-between;
	}
	.maincon .con{
		width: 50%;
	}
</style>
