<template>
  <div>
    <router-view
      class="view"
      keep-alive
      transition
      transition-mode="out-in">
    </router-view>
  </div>
</template>

<script>
  export default {}
</script>

<style>
  @import "./style/scss/style.scss";
</style>
