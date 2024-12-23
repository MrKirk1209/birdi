<template>
  <button class="primary-btn">
    {{ props.text }}
  </button>
</template>

<script setup>
const props = defineProps({
  text: {
    type: String,
    default: 'Продукция',
  }})
</script>
<style scoped>
.primary-btn {
  width: 100%;
  height: 48px; 
  background: transparent;
  border: 1px solid #598d66;
  color: #598d66; 
  font-family: 'Raleway', sans-serif;
  font-size: 16px;
  font-weight: 500;
  text-align: center;
  transition: background-color 0.3s, color 0.3s;
}

.primary-btn:hover {
  background-color: #598d66;
  color: #ffffff; 
}

</style>