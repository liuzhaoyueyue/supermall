<template>
	<div id="tab-bar-item" @click="handleClick">
		<div v-if="!active">
			<slot name="tab-img"></slot>
		</div>
		<div v-else>
			<slot name="tab-img-active"></slot>
		</div>
		<div :style="activeText">
			<slot name="tab-item"></slot>
		</div>
	</div>
</template>

<script>
export default {
	name: 'TabBarItem',
	data() {
		return {}
	},
	props: {
		path: String,
		color: {
			type: String,
			default: 'red',
		},
	},
	methods: {
		handleClick() {
			this.$router.push(this.path)
		},
	},
	computed: {
		active() {
			return this.$route.path.indexOf(this.path) !== -1
		},
		activeText() {
			return this.active ? { color: this.color } : {}
		},
	},
}
</script>

<style>
#tab-bar-item {
	flex: 1;
	text-align: center;
	font-size: 12px;
}
#tab-bar-item img {
	margin-top: 3px;
	height: 24px;
	width: 24px;
	vertical-align: middle;
}
</style>
