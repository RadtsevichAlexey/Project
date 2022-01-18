<template>
  <div id="app">
    <back-ground />

    <div class="logo-home">YouDiary</div>

    <div class="s_auto_reg">
      <h1>Authorization</h1>

      <form @submit.prevent="formSubmit">
        <div class="input_s_auto_reg">
          <input type="text" placeholder="login" v-model="form.login">
        </div>
        <div class="input_s_auto_reg">
          <input type="password" placeholder="password" v-model="form.password">
        </div>
        <div class="input_s_auto_reg">
          <router-link :to="{name: 'GeneralMain'}">
            <input type="submit" value="Enter">
          </router-link>
        </div>
      </form>
      <a>
        <router-link :to="{name: 'Registration'}" class="s_auto_reg_btn">Registration</router-link>
      </a>
    </div>
  </div>
</template>

<script>
import BackGround from '@/components/BackGround/BackGround.vue'

export default {
  name: 'Authorization',
  components: { BackGround },
  data () {
    return {
      form: {
        login: '',
        password: ''
      }
    }
  }
}

</script>

<style>

@import '../../styles/logs.css';
@import '../../styles/auto-reg.css';

</style>

  // methods: {
  //   async formSubmit () {
  //     const res = await fetch('http://localhost:', {
  //       method: 'POST',
  //       headers: {
  //         'Content-Type': 'application/json'
  //       },
  //       credentials: 'include',
  //       body: JSON.stringify ({
  //         login: this.form.login,
  //         password: this.form.password
  //       })
  //     })

  //     console.log(res)
  //   }
  // }
