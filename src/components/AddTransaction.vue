<script setup></script>

<template>
  <h3 class="text-xl font-semibold py-2 border-bottom shadow-md">
    Add New Transaction
  </h3>
  <div class="flex flex-col">
    <label class="text-xl py-2">Text</label>
    <input
      class="py-2 border border-gray-200 px-2 placeholder:text-gray-500"
      type="text"
      id="text"
      v-model="text"
      placeholder="Enter text..."
    />
  </div>
  <div class="flex flex-col py-4">
    <label class="text-lg py-2"
      >Amount <br />
      (negative-expense, positive-income)</label
    >
    <input
      class="placeholder:text-gray-500 py-2 px-2"
      type="number"
      v-model="amount"
      id="amount"
      placeholder="Enter amount..."
    />
  </div>
  <button class="bg-blue-500 text-white w-full py-2" type="submit" id="submit">
    Add Transaction
  </button>
</template>
