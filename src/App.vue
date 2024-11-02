<script setup>
import HeaderName from './components/HeaderName.vue'
import TotalBalance from './components/TotalBalance.vue'
import IncomeExpense from './components/IncomeExpense.vue'
import TransactionHistory from './components/TransactionHistory.vue'
import AddTransaction from './components/AddTransaction.vue'

// import { computed } from 'vue'

// const total = computed(() => {
//   return transactions.value.reduce((acc, transactions) =>{
//     return acc + transaction.amount;
//   }, 0);
// });
</script>

<template>
  <main class="flex items-center justify-center h-screen">
    <div class="flex flex-col px-2 w-4/12 py-4">
      <HeaderName />
      <TotalBalance :total="total" />
      <IncomeExpense :income="+income" :expenses="+expenses" />
      <TransactionHistory />
      <AddTransaction />
    </div>
  </main>
</template>
