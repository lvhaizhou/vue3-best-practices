<template>
  <button @click="toggle">click</button>
  <Heading level="5">hahah</Heading>
  <transition name="fade">
    <h1 v-if="showTitle">你好vue3</h1>
  </transition>
</template>

<script setup>
import { ref } from 'vue';
import Heading from '../components/test/Heading'

let showTitle = ref(true);
function toggle() {
  showTitle.value = !showTitle.value;
}


</script>


<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s linear;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>