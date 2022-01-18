<template>
  <div id="app">
    <back-ground />

    <div class="logo-home">YouDiary</div>

    <a>
      <router-link :to="{name: 'Authorization'}" class="start-btn">
        <span class="start-btn-line start-btn-line-top"></span>
        <span class="start-btn-line start-btn-line-right"></span>
        <span class="start-btn-line start-btn-line-bottom"></span>
        <span class="start-btn-line start-btn-line-left"></span>
        start now
      </router-link>
    </a>

  </div>
</template>

<script>
import BackGround from '@/components/BackGround/BackGround.vue'

export default {
  name: 'Home',
  components: { BackGround }
}
</script>

<style>

@import '../../styles/logs.css';
@import './start-button.css';

</style>
