<script setup>
import { RouterLink, RouterView } from 'vue-router'
import IconHome from './components/icons/IconHome.vue'
</script>

<template>
  <div class="grid grid-cols-2">
    <header>

      <div class="wrapper">

        <IconHome />
        <div class="greetings">
          <h1 class="green">{{ msg }}</h1>
          <h3>
            You’ve successfully created a project with
            <a target="_blank" href="https://vitejs.dev/">Vite</a> +
            <a target="_blank" href="https://vuejs.org/">Vue 3</a>.
          </h3>
        </div>

        <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/auth">Ingresar</RouterLink>
        </nav>
      </div>
    </header>
    <transition  name="fade" mode="out-in">
      <RouterView />
    </transition>
  </div>
</template>

<style >

</style>
