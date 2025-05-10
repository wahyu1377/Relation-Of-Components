<!-- components/HelloMessage.vue -->
<template>
  <div class="box">
    <h2>Halo, {{ name }}!</h2>
    <button @click="sendGreeting">Kirim Pesan ke Parent</button>
    <!-- Slot untuk konten dari parent -->
    <div class="slot-area">
      <slot />
    </div>
  </div>
</template>

<script setup>
const props = defineProps({ name: String }) // Props
const emit = defineEmits(['greet'])         // Emits

function sendGreeting() {
  emit('greet', `Salam dari ${props.name}`) // Emit event
}
</script>

<style scoped>
.box {
  border: 1px solid #ccc;
  padding: 1rem;
  border-radius: 10px;
}
.slot-area {
  margin-top: 1rem;
  padding: 0.5rem;
  background: #f9f9f9;
}
</style>



