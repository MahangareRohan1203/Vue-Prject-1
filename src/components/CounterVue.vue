<template>
    <div class="counter">
      <h1>Counter App</h1>
      <div class="count">{{ count }}</div>
      
      <button @click="decrement" :disabled="count === 0">Decrement</button>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const count = ref(0);
  
      const increment = () => {
        count.value++;
      };
  
      const decrement = () => {
        count.value--;
      };
  
      return { count, increment, decrement };
    }
  };
  </script>
  
  <style scoped>
  .counter {
    text-align: center;
    margin-top: 50px;
  }
  .count {
    font-size: 24px;
    margin-bottom: 20px;
  }

  button{
    margin:5px;
  }
  </style>
  