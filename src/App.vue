<!-- App.vue -->
<template>
  <div>
    <h1>Contoh Penggunaan Komponen di Vue </h1>

    <HelloMessage name="Wahyu" @greet="handleGreet">

      <p><em>Ini adalah konten dari parent yang masuk ke slot!</em></p>
    </HelloMessage>
  </div>
</template>

<script setup>
import HelloMessage from './components/HelloMessage.vue'

function handleGreet(pesan) {
  alert(pesan)
}
</script>
