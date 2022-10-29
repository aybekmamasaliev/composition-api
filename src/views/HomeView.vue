<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search">
    <p>Search term {{search}}</p>
    <div v-for="name in MatchingNames" :key="name">{{name}}</div>
    <button @click="handleClick">Stop watching</button>
  </div>
</template>

<script>
import {computed, ref, watch, watchEffect} from "vue"

export default {
  name: 'Home', 
  setup(){

    const search = ref("")

    const names = ref(["mario", "luigi" ,"yoshi", "brandon", "sandersan", "alp","aslan"])

    // const stopWatch = watch( search , ()=>{
    //   console.log("watch function ran")
    // })

    // const stopWatchEffect = watchEffect(()=>{
    //   console.log("watcheffect ran", search.value)
    // })

    const MatchingNames = computed(()=>{
      return names.value.filter(name => name.includes(search.value)) 
    })

    // const handleClick=()=>{
    //   stopWatch();
    //   stopWatchEffect();
    // }

    return { names, search, MatchingNames}
  }
}
</script>
