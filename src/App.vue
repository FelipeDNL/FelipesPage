<template>
  <div class="app-container">
    <Header />
    <div class="content">
      <HalfBox class="q1" style="flex: 1;" :isSelectable="true" @update="selectedInfo = $event">Quadro 1</HalfBox>
      <HalfBox class="q2" style="flex: 3;">{{ selectedInfo }}</HalfBox>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Header from './components/Header.vue';
import HalfBox from './components/HalfBox.vue';

const selectedInfo = ref('');
</script>

<style>
.app-container {
  display: flex;
  flex-direction: column;
  height: 95vh;
  width: 95vw;
}

.content {
  display: flex;
  flex-direction: row;
  flex: 1;
  gap: 10px;
}

.content>* {
  flex: 1;
}
</style>