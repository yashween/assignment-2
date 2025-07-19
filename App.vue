<template>
  <FloatingButton @toggle="menuVisible = !menuVisible" />
  <MenuPanel v-if="menuVisible" />

  <main style="padding: 2rem; max-width: 600px;">
    <h1>Accessibility Widget Demo</h1>
    <p>
      Welcome! This is some sample text. Try the Bigger Text toggle to see it grow,
      or enable the Contrast+ feature for higher contrast.
    </p>
    <p>
      Here’s a <a href="#">sample link</a> — turn on Highlight Links to make it stand out!
    </p>
    <img src="https://via.placeholder.com/400x200" alt="Test Image" />
    <p>
      If you click Hide Images, this image will disappear.
    </p>

    <div class="box"></div>
    <p>
      The blue box spins. Click Pause Animations to stop it!
    </p>
  </main>
</template>

<script setup>
import { ref } from 'vue'
import FloatingButton from './components/FloatingButton.vue'
import MenuPanel from './components/MenuPanel.vue'

const menuVisible = ref(false)
</script>

<style>
.box {
  width: 50px;
  height: 50px;
  background: blue;
  animation: spin 2s linear infinite;
  margin-top: 20px;
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
</style>
