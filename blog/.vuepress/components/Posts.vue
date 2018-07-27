<template>
    <div>
        <ul>
            <li v-for="post in posts">
                <!-- {{getUrlPost(post.id)}} -->
                <a :href="getUrlPost(post.id)">{{post}}</a>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    data(){
        return{
            posts: {},

        }
    },
    mounted(){
        fetch("https://jsonplaceholder.typicode.com/posts/")
            .then(response=>response.json())
            .then(data => this.posts = data)
            .catch(error=>alert(error))
    },
    methods:{
        getUrlPost(id){
            let objeto = this.posts.filter(post=>post.id===id);
            return `/post/${objeto[0].id}`;
        }
    }
}
</script>

