<script>
    export default{
        data(){
            return{
                links: [ 
            {
                label: 'CHARACTERS',
                active: false
            },
            {
                label: 'COMICS',
                active: true
            },
            {
                label: 'MOVIES',
                active: false
            },
            {
                label: 'TV',
                active: false
            },
            {
                label: 'GAMES',
                active: false
            },
            {
                label: 'COLLECTIBLES',
                active: false
            },
            {
                label: 'VIDEOS',
                active: false
            },
            {
                label: 'FANS',
                active: false
            },
            {
                label: 'NEWS',
                active: false
            },
            {
                label: 'SHOP',
                active: false
            },
        ]
            }
        }
            
    }
</script>
<template>
    <div class="bg-white">
        <div class="container">
            <a href="/">
                <img src="../assets/img/dc-logo.png" alt="logo">
            </a>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a href="#" :class="link.active ? 'active' : ''">
                        {{ link.label }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
        @use '../styles/partials/variables' as *;
    .bg-white{
        background-color: #fff;
    }

    .container{
        max-width: 1170px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        img{
            padding: 10px;
            width: 90px;
        }
        ul{
            list-style-type: none;
            li{
                display: inline-block;
                margin: 0 10px;
                
            }
            a{
                text-decoration: none;
                color: #000;
                font-size: 10px;
                padding: 34px 0;
                &:hover{
                    color: $color;
                    border-bottom: 3px solid $color;
                }
            }
        }
        .active{
            color: $color;
            border-bottom: 3px solid $color;
        }
    }
    
</style>