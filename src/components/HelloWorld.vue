<template>
  <div class="alert alert-info">
    <h2>{{ title }}</h2>
    <p ref="msg">{{ message }}</p>
    <div>
      <button class="btn btn-primary" v-on:click="doAction">Click!</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      title: 'HelloWorld',
      message: 'This is sample message.',
    }
  },
  mounted() {
    this.counter = 0
  },
  methods: {
    doAction() {
      this.counter++
      this.$refs.msg.innerHTML += '<h6>counted: ' + String.fromCharCode(64 + this.counter) + '</h6>'
    }
  }
}
</script>
