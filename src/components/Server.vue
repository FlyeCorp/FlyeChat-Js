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
	background-color: #01010225;
	color: white;
	display: flex;
	align-items: center;
	margin-top: 3px;
	padding: 5px;
	border-radius: 5px;
	cursor: pointer;
	user-select: none;
	overflow-x: hidden;
	text-overflow: ellipsis;
	white-space: nowrap;
}

div:hover {
	background: #35384d93;
}

img {
	width: 35px;
	height: 35px;
	object-fit: cover;
	border-radius: 7px;
}

h1 {
	font-size: 14px;
	margin-left: 5px;
}

</style>