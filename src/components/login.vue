<script setup>
import axios from 'axios';

export default {
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    async login() {
      try {
        const response = await axios.post('https://jurapro.bhuser.ru/api-shop/login', {
          email: this.email,
          password: this.password,
        });

        console.log(response.data);
      } catch (error) {
        console.error('Login failed:', error.response ? error.response.data : error.message);
      }
    },
  },
};
</script>

<template>
  <div class="container mt-5">
    <h4>Login</h4>
    <form @submit.prevent="login" class="mt-3">
      <label for="email">E-Mail Address</label>
      <div>
        <input id="email" type="email" v-model="email" required>
      </div>
      <label for="password">Password</label>
      <div>
        <input id="password" type="password" v-model="password" required>
      </div>
      <div class="mt-3">
        <button type="submit" class="btn btn-primary">Login</button>
      </div>
    </form>
  </div>
</template>

<style scoped>

</style>