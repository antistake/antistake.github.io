<script setup>
import { ref } from 'vue'
import './Feature.vue'
import Feature from './Feature.vue';
import Networks from './Networks.vue';
import Footer from './Footer.vue';

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>
  <h3 style="opacity: 70%">A secure staking service for the Dotsama ecosystem</h3>

  <Feature />

  <Networks />
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');
h1 {
  font-family: Lobster;
}
</style>
