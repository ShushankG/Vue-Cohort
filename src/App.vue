<template>
  <div>
    <h1>DC Heroes</h1>
    <ul>
      <li v-for="hero in name" :key="hero">
        {{ hero }}
      </li>
    </ul>
    <button :disabled="isActive">Add Hero</button>
    <input type="text" v-model="newHero" :disabled="isActive">
   <div> <textarea v-model.lazy="textInput"></textarea></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: ["superman", "batman", "flash"],
      isActive:false,
      newHero:"Hero-Name",
      textInput:""
    };
  }
};
</script>

<style>
/* Add your styles here */
</style>
