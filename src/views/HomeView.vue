<template>
  <div class="home">
    <Counter />

    <div class="buttons">
      <button @click="counterStore.decrement">-</button>
      <button @click="counterStore.increment">+</button>
    </div>

    <hr>

    <div>
      This counter value is: {{ counterStore.oddOrEven }}
    </div>

    <hr>

    <div>
      Edit Count:
      <input type="number" v-model="counterStore.count">
    </div>
  </div>
</template>

<script setup>
  import Counter from '@/components/Counter.vue';
  import { useCounterStore } from '@/stores/counter';

  const counterStore = useCounterStore();

</script>

<style>
.buttons {
  font-size: 40px;
  margin: 10px;
}
</style>