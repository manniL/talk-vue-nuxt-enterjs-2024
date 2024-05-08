<script setup lang="ts">
import { onBeforeUnmount } from 'vue'

const audio = new Audio('./crickets.wav');

const toggle = () => {
  if (audio.paused) {
    audio.play();
  } else {
    audio.pause();
  }
}

onBeforeUnmount(() => {
  audio.pause();
})

</script>

<template>
  <button @click="toggle">
    <slot />
  </button>
</template>