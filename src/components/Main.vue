<template>
  <div class="main">
    <div class="main__header">
      <h1>HEADER!!!</h1>
    </div>
    <div class="main__settings">
      setting, navigate menu list
    </div>
    <div class="main__content">
      <Posts/>
    </div>
  </div>
</template>

<script>
import Posts from './Posts'

export default {
  name: "Main",
  components: {Posts},

}
</script>

<style lang="scss">
.main {

  &__header {
    text-align: center;
  }

  &__settings {
    width: 30%;
    float: left
  }

  &__content {
    width: 70%;
    float: right
  }
}
</style>