<template>
    <div class="app">
        <postForm
        @create="createPost"
        />
        <postList 
        :posts="posts"
        />

        <!-- <div>
            <button @click="addLike">Like</button>
            <button @click="addDislike">Dislike</button>
        </div>
        <div>Кол-во лайков: <strong> {{ likes }} </strong></div>
        <div>Кол-во дизлайков: <strong> {{ dislikes }} </strong></div> -->



        </div>

</template>

<script>
import PostForm from "@/components/PostForm"
import PostList from "@/components/PostList"
export default {
    components: {
        PostList, PostForm
    },
    data(){
        return {
            posts: [
                {id: 1, title: 'Javascipt', body: 'Описание поста'},
                {id: 2, title: 'Javascipt 2', body: 'Описание поста 2'},
                {id: 3, title: 'Javascipt 3', body: 'Описание поста 3'},
                {id: 4, title: 'Javascipt 4', body: 'Описание поста 4'},
            ],
        }
    },
    methods: {
        createPost(post){
            this.posts.push(post);
        },
    } 
}

</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.app{
    padding: 20px;
}


</style>