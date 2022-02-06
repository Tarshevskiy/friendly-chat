<template>
  <div class="chat-window" @click.self="resetChatSize">
    <textarea v-model="message"  @keydown.enter.exact="sendMessage" @keyup.enter.exact="message = ''" placeholder="Type..."/>
  </div>
</template>

<script>
export default {
  name: 'Chat',
  data() {
    return {
      height: null,
      width: null,
      message: ''
    }
  },
  methods: {
    sendMessage(e){
      this.message = e.target.value;
      e.target.value = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.chat-window{
  height: 100vh;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  background-color: aqua
}

</style>
