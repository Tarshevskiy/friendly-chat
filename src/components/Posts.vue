<template>
<div class="posts">
  <textarea v-model="text" placeholder="Type..."></textarea>
  <button @click="addPost" :disabled=!text>Add post</button>
  <div v-for="item in list" :key="item.createdAt">
    <div>{{ item.text }}</div>
  </div>
</div>
</template>

<script>
import moment from "moment";

export default {
  name: "Posts",
  data(){
    return {
      list: [{text: 'make tea', id: 0}, {text: 'go sleep', id: 1}],
      text: null
    }
  },
  methods: {
    addPost() {
      this.list.push({
        text: this.text,
        createdAt: moment().format("DD.MM.YY"),
        id: 3
      })
      this.text = null
    }
  }
}
</script>

<style scoped>
.posts{
  display: flex;
  flex-direction: column;
}
</style>