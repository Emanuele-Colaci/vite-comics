<script>
    export default {
        props:{
            img: String,
            price: Number,
            series: String,
            type: String
        }
    }
</script>
<template>
    <div>
        <img :src="img">
        <h3>{{ series }}</h3>
    </div>
</template>
<style lang="scss" scoped>
    div{
        width: calc(100% / 6 - 20px);
        margin: 10px;
        img{
            object-fit: cover;
            width: 100%;
            height: 80%;
        }
        h3{
            margin-top: 10px;
            color: #fff;
            font-size:0.8rem;
        }
    }
</style>