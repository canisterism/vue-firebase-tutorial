<template>
  <div class="login">
    <h3>Sign In</h3>
    <input type="text" placeholder="Email">
    <input type="password" placeholder="Password">
    <button v-on:click="login">Connection</button>
    <p>You don't have account? You can <router-link to="/sign-up">create one</router-link></p>
  </div>
</template>

<script>
export default {
  name: 'login',
  data: function () {
    return {}
  },
  methods: {
    login: function () {
      this.$router.replace('hello-world')
    }
  }
}
</script>

<style scoped>
  .login {
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
    margin-top: 40px;
    font-size: 13px;
  }
  p a {
    text-decoration: underline;
    cursor: pointer;
  }
</style>
