<template>
  <Servers :servers="servers" />
</template>

<script>
import Servers from './components/Servers'

export default {
  name: 'App',
  components: {
    Servers,
  }, 
  data() {
    return {
      servers: [],
      }
    },
    methods: {
      async fetchServers() {
        const res = await fetch("http://localhost:5000/servers")

        const data = await res.json()

        return data
      },
      async fetchChannels() {
        const res = await fetch("http://localhost:5000/channels")

        const data = await res.json()

        return data
      }
    },
    async created() {
      this.servers = await this.fetchServers()

    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #1B1C27;
  margin: 0;
  padding: 0;
}

.title {
  margin: 10px;
  text-align: center;
  color: white;
  font-size: 25px;
}
</style>
