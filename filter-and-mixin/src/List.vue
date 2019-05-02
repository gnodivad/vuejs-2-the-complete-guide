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
export default {
  data() {
    return {
      fruits: ["Apple", "Banana", "Mango", "Melon"],
      filterText: ""
    };
  },
  computed: {
    filteredFruits() {
      return this.fruits.filter(fruit => {
        return fruit.match(this.filterText);
      });
    }
  }
};
</script>

<style>
</style>
