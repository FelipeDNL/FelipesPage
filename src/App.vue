<script setup>
import Header from './components/Header.vue';
import HalfBox from './components/HalfBox.vue';
</script>

<template>
  <div class="app-container">
    <Header />
    <div class="content">
      <HalfBox class="q1" style="flex: 1;">Quadro 1</HalfBox>
      <HalfBox class="q2" style="flex: 3;">Quadro 2</HalfBox>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import HalfBox from './components/HalfBox.vue';

export default {
  components: {
    Header,
    HalfBox,
  },
};
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

.content > * {
  flex: 1;
}
</style>