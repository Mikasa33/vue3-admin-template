<script setup lang="ts">
  import { getDemo } from '/@/service/demo';

  const { data, error, isLoading, isFinished } = getDemo({ id: 2 });
  console.log(data, error);
</script>

<template>
  <div class="fail flex-center flex-col">
    <h1 class="text-black dark:text-white">This is an fail page</h1>
    <div>loading: {{ isLoading.toString() }}</div>
    <div>finished: {{ isFinished.toString() }}</div>
    <pre>{{ JSON.stringify(data) }}</pre>
    <pre>{{ error }}</pre>
  </div>
</template>
