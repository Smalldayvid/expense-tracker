<script setup>
defineProps({
  balance: {
    type: Number,
    default: 0,
    required: true,
  },
})
</script>

<template>
  <div class="font-semibold py-2">
    <h3 class="text-xl tracking-tight">YOUR BALANCE</h3>
    <label class="text-4xl">$ {{ balance }}</label>
  </div>
</template>
