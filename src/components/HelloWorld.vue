<template>
  <div class="alert alert-info">
    <h2>{{ title }}</h2>
    <p>{{ message }}</p>
    <hr>
    <p class="h5">val: {{ val }}</p>
    <div class="form-group text-left">
      <label>value:</label>
      <input type="number" v-model="val" class="form-control">
    </div>
    <table class="bg-white table mt-4">
      <tr><th>add:</th><td>{{ add }}</td></tr>
      <tr><th>sub:</th><td>{{ sub }}</td></tr>
      <tr><th>mult:</th><td>{{ mult }}</td></tr>
      <tr><th>divide:</th><td>{{ div }}</td></tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      title: 'Watcher',
      message: 'ウォッチャー',
      val: 0,
      add: 0,
      sub: 0,
      mult: 0,
      div: 0,
    }
  },
  watch: {
    val(newV, oldV) {
      console.log(oldV + ' => ' + newV)
      this.val = newV
      let val = parseInt(this.val)
      this.add = Math.floor(val + 2)
      this.sub = Math.floor(val - 2)
      this.mult = Math.floor(val * 2)
      this.div = Math.floor(val / 2)
    }
  },
  created() {
    this.val = 6
  },
  // render() {
  //   return h('div', {
  //     class: 'alert alert-warning'
  //   },
  //   [
  //     h('h2', this.title),
  //     h('p', this.message)
  //   ])
  // }
}
</script>
