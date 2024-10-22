<template>
  <div id="app">
    <HelloWorld title="computed" />
  </div>
</template>

<script>
// import HelloJSX from './components/helloJSX';
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data() {
    return {
      message: 'validate',
      num: 123,
    }
  }
}
</script>
