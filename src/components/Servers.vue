<template>
	<div :key="server.id" v-for="server in servers">
		<server :server="server"/>
	</div>
</template>

<script>
	import Server from './Server'

	export default {
		name: 'Server List',
		props: {
			servers: Array
		},
		components: {
			Server
		}
	}
</script>