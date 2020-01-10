<template>
  <div id="app">
    <p>{{ val }}</p>
    <button @click="val = 5">Click to change</button>
  </div>
</template>

<script>

export default {
  data() {
    return {
      val: "world",
      counter: 0
    }
  },
  beforeCreate() {
    alert('Hello ' + this.val + ' ' + 'I come first')
  },
  created() {
    alert('Hello ' + this.val + ' ' + 'I come second')
  },
  beforeMount() {
    alert('Hello ' + this.$el + ' ' + 'I come third')
  },
  mounted() {
    alert('Hello this is: ' + this.$el.textContent + ' I come fourth')
  },
  beforeUpdate() {
    alert("beforeUpdate() counter is: " + this.val)
  },
  updated() {
    alert("updated() val is now: " + this.val)
  },
  destroyed() {
    alert("now destroyed " + this.val)
  }

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
