<template>
    <img :src="avatar" alt="avatar" id="avatar">
</template>
<script>
export default {
    data(){
        return{

        }
    },
    computed:{
        avatar(){
            return `https://www.gravatar.com/avatar/97c1fbe0453cfdc5a5582cf0f8dbdbfe`
        }
    }
}
</script>
<style scoped>
#avatar{
    border-radius: 40%;
}
</style>

