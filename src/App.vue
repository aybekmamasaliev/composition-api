<template>
  <div class="home">
    <nav>
      <router-link to="/">1</router-link> |
      <router-link to="/second">2</router-link>
    </nav>
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ninjaOne.name}} - {{ninjaOne.age}}</p>
    <p>{{ninjaTwo.name}} - {{ninjaTwo.age}}</p>
    <p>{{nameone}}</p>
    <p>{{nametwo}}</p>
    <button @click="updateNinjaOne">Update</button>
    <button @click="updateNinjaTwo">Update</button>
  </div>
  <router-view />
</template>

<script>

import { ref, reactive } from "vue"
export default {
  name: "Home",
  setup() {
    const ninjaOne = ref({name:"Marios", age:30})
    const ninjaTwo = reactive({name:"Luigi", age:33})
    const updateNinjaOne=()=>{
      ninjaOne.value.age = 40
      ninjaOne.value.name = "shaun"
    }

    const updateNinjaTwo=()=>{
      ninjaTwo.age = 40
      ninjaTwo.name = "shaun"
    }
    return { ninjaOne, ninjaTwo, updateNinjaOne, updateNinjaTwo}
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.test {
  color: red;
}
</style>
