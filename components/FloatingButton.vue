<template>
  <button class="floating-btn" @click="$emit('toggle')">
    ⚙️
  </button>
</template>

<style scoped>
.floating-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background: #333;
  color: #fff;
  border: none;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  font-size: 24px;
  cursor: pointer;
}
</style>
