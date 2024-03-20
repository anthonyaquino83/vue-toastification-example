<script setup>
import { useRouter } from 'vue-router'
import { useToast } from 'vue-toastification'

const router = useRouter()
const toast = useToast()

function goToAbout() {
  router.push('/about')
}
function showToast(isSuccess = true) {
  if (isSuccess) {
    toast.info("I'm an info toast!")
  } else {
    toast.error("I'm an error toast!")
  }
}
</script>

<template>
  <h2>HomeView</h2>
  <div class="div" style="margin-bottom: 8px">
    <button @click="goToAbout">Go to About</button>
  </div>
  <div class="div" style="margin-bottom: 8px">
    <button @click="showToast">Show Toast</button>
  </div>
  <div class="div" style="margin-bottom: 8px">
    <button @click="showToast(false)">Show Error Toast</button>
  </div>
</template>
