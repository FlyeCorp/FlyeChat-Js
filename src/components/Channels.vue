<template>
    <div id="channel-list" class="container">
        <h2 class="channel-header">Text Channels</h2>
        <TextChannels />
    </div>
</template>

<script>
import TextChannels from './TextChannel'

export default {
	name: 'Channel List',
    props: {
    textchannel: Array,
  },
  components: {
    TextChannels,
  },
}
</script>

<style scoped>
.container {
  width: 200px;
  padding: 5px;
  background: #1f202c;
  overflow-x: hidden;
  overflow-y: scroll;
  filter: drop-shadow(0px 0px 5px rgba(0, 0, 0, 0.164));
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