<template>
    <main>
        <h3>Lista post</h3>

        <PostItem 
            v-for="post in posts"
            :key="post.id"
            :post="post"
        />

    </main>
</template>

<script>
import PostItem from './partials/PostItem';

export default {
    name: 'Posts',

    components: {
        PostItem,
    },
    
    data(){
        return {
            apiUrl: 'http://127.0.0.1:8000/api/posts',
            posts: null
        }
    },
    
    mounted(){
        this.getPosts();
    },

    methods: {
        getPosts(){
           // console.log(axios);
           axios.get(this.apiUrl)
            .then(res => {
                this.posts = res.data;
                console.log(this.posts);
            })
        }
    }
}
</script>

<style lang="scss" scoped>
    main{
        padding: 30px;
        h3 {
            margin-bottom: 30px;
        }
    }

</style>