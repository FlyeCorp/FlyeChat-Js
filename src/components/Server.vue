<template>
	<div>
		<img :src="server.image" :alt="server.name">
		<h1>{{server.name}}</h1>
	</div>
</template>

<script>
export default {
	name: 'server',
	props: {
		server: Object,
	},
}
</script>

<style scoped>

div {
	background-color: rgb(51, 50, 59);
	color: white;
	display: flex;
}

img {
	width: 100px;
	height: 100px;
	object-fit: cover;
}

</style>