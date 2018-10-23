<template>
  <div class="sign-up">
    <h3>Let's create a new account!</h3>
    <input type="text" placeholder="Email">
    <input type="password" placeholder="Password">
    <button>Sign Up</button>
    <span>Or go back to <router-link to="/login">login</router-link>.</span>
  </div>
</template>

<script>
export default {
  name: 'signUp',
  data: function () {
    return {}
  },
  methods: {}
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
