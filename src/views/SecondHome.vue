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
            {title: "welcome to the blog", body:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.", id:1},
            {title:"top 5 css tips", body: "lorem Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum." , id:2}
        ])

        return{ posts }
    }


}
</script>

<style>

</style>