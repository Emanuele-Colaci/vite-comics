<script>
    export default {
        data(){
            return{
                images: [ 
                    {
                        image: '/src/assets/img/buy-comics-digital-comics.png',
                        link: '#',
                        label: 'DIGITAL COMICS'   
                    },
                    {
                        image: '/src/assets/img/buy-comics-merchandise.png',
                        link: '#',
                        label: 'DC MERCHANDISE'   
                    },
                    {
                        image: '/src/assets/img/buy-comics-subscriptions.png',
                        link: '#',
                        label: 'SUBSCRIPTION'   
                    },
                    {
                        image: '/src/assets/img/buy-comics-shop-locator.png',
                        link: '#',
                        label: 'COMIC SHOP LOCATOR'   
                    },
                    {
                        image: '/src/assets/img/buy-dc-power-visa.svg',
                        link: '#',
                        label: 'DC POWER VISA', 
                        isSvg: true  
                    },
        
                ]
            }
        }
    }
</script>
<template>
    <div>
        <div class="bg-blue">
        <div class="container1 content1">
            <a v-for="(image, index) in images" :key="index" :href="image.link">
                <img :src="image.image" :class="{ 'svg-img': image.isSvg } ">
                <span>{{ image.label }}</span>
            </a>
        </div>
    </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
     .bg-blue{
        background-color: $color;
        padding: 20px;
    }
    .container1{
        max-width: 1170px;
        margin: 0 auto;
    }
    .content1{
        display: flex;
        justify-content: center;
        align-items: center;
        img{
            width: calc(100% / 5 );
            margin: 20px;
            vertical-align: middle;
        }
        a{
            text-decoration: none;
            color: #fff;
            font-size: 10px;
            span{
                margin-left: 5px;
            }
        }
        .svg-img {
            width: 60px; /* Imposta la larghezza desiderata per l'immagine SVG */
        }
    }
</style>