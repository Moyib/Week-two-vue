<template>
  <div id="app">
    <form @click.prevent="submitForm">
      <label for="firstname">
        First Name:
        <input id="firstname" type="text" v-model="firstName" placeholder="Your first name here">
      </label><br>
      <label for="lastname">
        Last Name: 
        <input id="lastname" type="text" v-model="lastName" placeholder="Your last name here">
      </label><br>
      
      <p> {{ fullName }} </p>
    </form>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      firstName: "",
      lastName: "",
    }
  },
  computed: {
    fullName: function() {
      return this.firstName + ' ' + this.lastName
    },
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
