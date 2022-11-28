<script>
import WelcomeItem from './WelcomeItem.vue'
export default {
  props: ['foo'],
  created() {
    // props are exposed on `this`
    console.log(this.foo)
  }
}
</script>

<template>
  <WelcomeItem>
    <h1>THE CARDD WHOAAA</h1>
  </WelcomeItem>
</template>
