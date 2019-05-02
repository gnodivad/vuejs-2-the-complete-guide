<template>
  <div>
    <h1>Filters & Mixins</h1>
    <input v-model="filterText" />
    <ul>
      <li :key="index" v-for="(fruit, index) in filteredFruits">
        {{ fruit }}
      </li>
    </ul>
  </div>
</template>

<script>
import { fruitMixin } from "./fruitMixin";
export default {
  mixins: [fruitMixin]
};
</script>

<style>
</style>
