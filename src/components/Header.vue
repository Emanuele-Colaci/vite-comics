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
            <img src="../img/dc-logo.png" alt="logo">
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
        max-width: 1024px;
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
                &:hover{
                    color: $color;
                }
            }
        }
        .active{
            color: $color;
            position: relative;
            
            &:after{
                display: block;
                content: '';
                background-color: $color;
                height: 3px;
                width: 50%;
                position: absolute;
                right: 25%;
                bottom: -39px;
                transform: translatey(-50%);
            }
        }
    }
    
</style>