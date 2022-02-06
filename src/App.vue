<template>
  <div>
  <Main :list="list" />
  </div>
</template>

<script>

import Main from './components/Main'

export default {
  name: 'App',
  components: {
    Main
  },
  data(){
    return {
      list: [{message: 'make tea', id: 0}, {message: 'go sleep', id: 1}]
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
</style>
