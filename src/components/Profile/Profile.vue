<template>
  <div id="app">

    <navbar />

    <div class="profile-box">
      <div class="profile-text" id="user">

        {{user_info}}

        <p>
          Login:<br/>
          <output>Alex</output>
        </p>
        <p>
          Name:<br/>
          <output>Alexey</output>
        </p>
        <p>
          Height:<br/>
          <output>180</output>
        </p>
        <p>
          Weight:<br/>
          <output>100</output>
        </p>
        <p>
          Sex:<br/>
          <output>male</output>
        </p>
        <p>
          Age:<br/>
          <output>20</output>
        </p>
      </div>
    </div>

    <router-link :to="{name: 'Authorization'}">
      <div class="profile-style-out">
        <a class="buttons_style">
          Sign Out
        </a>
      </div>
    </router-link>

    <div class="profile-style-edit">
        <a class="buttons_style">
          Edit
        </a>
    </div>

  </div>
</template>

<script>
import Navbar from '@/components/Navbar/Navbar.vue'
import Vue from 'vue'

export default {
  name: 'Profile',
  components: {
    Navbar
  },
  el: '#user',
  data() {
    return {
      user_info: null
    };
  },
  mounted() {
    axios
      .get('https://localhost:7223/users')
      .then(response => (this.info = response));
  }
}

</script>

<style>

@import './profile-style.css';
@import '../../styles/buttons-style.css';

</style>
