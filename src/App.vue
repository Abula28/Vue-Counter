
<template>
  <div class="something">
    <HeaderComponent />

</div>
</template>

  <script setup>
  import HeaderComponent from './components/header.vue'

  </script>

<style scoped>
.something{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 1024px) {
  
}
</style>
