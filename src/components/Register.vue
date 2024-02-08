<script setup>
import axios from 'axios';

export default {
  data() {
    return {
      name: '',
      email: '',
      password: '',
      password_confirmation: '',
      is_admin: null,
    }
  },
  methods: {
    async register() {
      try {
        const response = await axios.post('https://jurapro.bhuser.ru/api-shop/register', {
          name: this.name,
          email: this.email,
          password: this.password,
          password_confirmation: this.password_confirmation,
          is_admin: this.is_admin,
        });
        console.log(response.data);
      } catch (error) {
        console.error('Registration failed: ', error.response ? error.response.data : error.message);
      }

    }
  }
};
</script>

<template>
  <div class="container mt-5">
    <h4>Register</h4>
    <form @submit.prevent="register" class="mt-3">>
      <label for="name">Name</label>
      <div>
        <input id="name" type="text" v-model="name" required autofocus>
      </div>
      <label for="email">E-Mail Address</label>
      <div>
        <input id="email" type="email" v-model="email" required>
      </div>
      <label for="password">Password</label>
      <div>
        <input id="password" type="password" v-model="password" required>
      </div>
      <label for="password-confirm">Confirm Password</label>
      <div>
        <input id="password-confirm" type="password" v-model="password_confirmation" required>
      </div>
      <div class="mt-3">
        <button type="submit" class="btn btn-primary">Register</button>
      </div>
    </form>
  </div>
</template>

<style scoped>

</style>