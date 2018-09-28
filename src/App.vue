<template>
  <div id="app">
    <Profile name="Rita Costa" imgSrc="https://via.placeholder.com/100x100" />
  </div>
</template>

<script>

import Profile from './components/Profile/Profile.vue'

export default {
  name: 'app',
  components: {
    Profile
  }
}
</script>

<style lang="scss">
@import 'assets/style.scss';
</style>
