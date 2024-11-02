<script setup>
defineProps({
  transaction: {
    type: Array,
    required: true,
  },
})
const emit = defineEmits(['transactionDeleted'])

const deleteTransaction = id => {
  emit('transactionDeleted', id)
}
</script>

<template>
  <div class="py-6 font-semibold text-xl">
    <h3 class="border-bottom shadow-md py-2">History</h3>
    <ul id="list" class="list">
      <li
        v-for="transaction in transactions"
        :key="transaction.id"
        class="transaction.amount < 0 ? 'minus' : 'plus'"
      >
        {{ transaction.text }} <span>${{ transaction.amount }}</span>
        <button @click="deleteTransaction(transaction.id)" class="delete-btn">
          x
        </button>
      </li>
    </ul>
  </div>
</template>
