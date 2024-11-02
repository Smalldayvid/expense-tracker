<script setup>
import { defineProps } from 'vue'

defineProps({
  income: {
    type: Number,
    default: 0,
    required: true,
  },
  expenses: {
    type: Number,
    default: 0,
    required: true,
  },
})
</script>

<template>
  <div
    class="border divide-x-2 > * + * flex box-border gap-4 justify-center shadow-md py-4"
  >
    <div class="py-2 justify-center items-center px-12">
      <h4 class="font-semibold">INCOME</h4>
      <label id="money-minus" class="money plus text-green-500"
        >+${{ income }}</label
      >
    </div>
    <div class="py-2 justify-center items-center px-12">
      <h4 class="font-semibold">EXPENSE</h4>
      <label id="money-minus" class="money minus text-red-500"
        >-${{ expenses }}</label
      >
    </div>
  </div>
</template>
