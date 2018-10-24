<template>
  <div class="sign-up">
    <h3>Let's create a new account!</h3>
    <input type="text" placeholder="Email" v-model="email">
    <input type="password" placeholder="Password" v-model="password">
    <button v-on:click="signUp">Sign Up</button>
    <span>Or go back to <router-link to="/login">login</router-link>.</span>
  </div>
</template>

<script>

import firebase from 'firebase'

export default {
  name: 'signUp',
  data: function () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    signUp: function () {
      firebase.auth().createUserWithEmailAndPassword(this.email, this.password).then(
        (user) => {
          this.$router.replace('hello-world')
        },
        (err) => {
          alert('Oops.' + err.message)
        }
      )
    }
  }
}
</script>

<style scoped>
  .signUp {
    margin-top: 40px;
  }
  input {
    display: block;
    margin: 10px auto;
    width: 20%;
    padding: 15px;
  }
  button {
    margin-top: 20px;
    width: 10%;
    cursor: pointer;
  }
  p {
    margin-top: 10px;
    width: 20%;
    padding: 15px;
  }
  span {
    display: block;
    margin-top: 20px;
    font-size: 11px;
  }
</style>
