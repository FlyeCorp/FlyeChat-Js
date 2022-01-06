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
      servers: []
      }
    },
    created() {
      this.servers = [
        {
          id: 1,
          name: 'Dank Empire',
          image: 'https://picsum.photos/200/100',
          imageXoffset: 50,
        },
        {
          id: 2,
          name: 'Langley Dickheads',
          image: 'https://picsum.photos/200/500',
          imageXoffset: 50,
        },
        {
          id: 3,
          name: 'FlyeChat Main Server',
          image: 'https://picsum.photos/200/300',
          imageXoffset: 50,
        },
      ]

    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
