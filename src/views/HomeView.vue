<template>
  <div class="home">
    <div class="count">
      {{ counterStore.count }}
    </div>

    <div class="buttons">
      <button @click="counterStore.decrement">-</button>
      <button @click="counterStore.increment">+</button>
    </div>

    <hr>

    <div>
      This counter value is: {{ counterStore.oddOrEven }}
    </div>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter';

  const counterStore = useCounterStore();

</script>

<style>
.count {
  font-size: 60px;
  margin: 20px;
}

.buttons {
  font-size: 40px;
  margin: 10px;
}
</style>