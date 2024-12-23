<script setup>
import { RouterView } from 'vue-router'
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
</script>

<template>
  <div class="">
    <header>
      <HeaderComponent></HeaderComponent>
    </header>

      <RouterView />

    <FooterComponent></FooterComponent>
  </div>
</template>

<style src="@/assets/main.css">
</style>
