<template>
  <div class="container">
    <h1 class="title">FlyeChat</h1>
    <div :key="server.id" v-for="server in servers">
      <server :server="server" />
    </div>
  </div>
</template>

<script>
import Server from "./Server";

export default {
  name: "Server List",
  props: {
    servers: Array,
  },
  components: {
    Server,
  },
};
</script>

<style scoped>
.container {
  width: 200px;
  padding: 5px;
  background: #1f202c;
  overflow-x: hidden;
  overflow-y: scroll;
  z-index: 2;
  filter: drop-shadow(0px 0px 5px rgba(0, 0, 0, 0.363));
}

::-webkit-scrollbar {
  width: 3px;
}
  ::-webkit-scrollbar-track {
  background: transparent; 
}
  ::-webkit-scrollbar-thumb {
  background: rgb(89, 94, 165); 
    border-radius:10px;
}
::-webkit-scrollbar-thumb:hover {
  
  background: #555; 
} 
</style>