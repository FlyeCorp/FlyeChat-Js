<template>
	<div>
		<h1>{{textchannel.name}}</h1>
	</div>
</template>

<script>
export default {
	name: 'textchannel',
	props: {
		server: Object,
	},
}
</script>

<style scoped>

div {
	background-color: #1B1C2766;
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