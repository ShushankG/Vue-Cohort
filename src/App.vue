

<template>
  <div>
    <h1>DC Heroes</h1>
    <ul>
      <li v-for="(hero,index) in name" :key="hero">
        {{ hero }}
    <button @click="clearHero(index)" :disabled="isActive">X</button>
      </li>
    </ul>
    <input type="text" v-model="newHero" :disabled="isActive">
    <button @click="addhero" :disabled="isActive">Add Hero</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: ["superman", "batman", "flash"],
      isActive:false,
      newHero:"",
    };
  },
  methods:{
addhero(){
if(this.newHero!=""){
  this.name.push(this.newHero);
}
},
clearHero(index){
// this.name=this.name.filter((val)=>{ return val!=hero});
this.name.splice(index, 1,"deleted");
}
  }
};
</script>

<style>
/* Add your styles here */
</style>
