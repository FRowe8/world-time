<script setup lang="ts">
import DarkSwitcher from './components/DarkSwitcher.vue'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <div font-sans bg-canvas h-screen>
    <NavBar />
    <div border="~ base rounded" bg-base shadow m2>
      <ActionBar />
      <TimeSchedular />
    </div>
  </div>
</template>

<style>
html.dark {
  background: #222;
  color: white;
  color-scheme: dark;
}
</style>
