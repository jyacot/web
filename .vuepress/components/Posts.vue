<template>
    <div>
        <ul>
            <li v-for="post in posts">
                {{post}}
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
    }
}
</script>

