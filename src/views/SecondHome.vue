<template>
  <h1>Home 2</h1>
  <PostList :posts="posts"/>
</template>

<script>
import PostList from "../components/PostListView.vue"
import { ref } from "vue"
export default {
    name:"SecondHome",
    components:{PostList},
    setup(){
        const posts = ref([
            {title: "welcome to the blog", body:"Lorem ipsum", id:1},
            {title:"top 5 css tips", body: "lorem ipsum" , id:2}
        ])

        return{ posts }
    }


}
</script>

<style>

</style>