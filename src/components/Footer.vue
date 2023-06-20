<script>
    export default{
        data(){
            return{
                images: [ 
                    {
                        image: '/src/img/buy-comics-digital-comics.png',
                        label: 'DIGITAL COMICS'   
                    },
                    {
                        image: '/src/img/buy-comics-merchandise.png',
                        label: 'DC MERCHANDISE'   
                    },
                    {
                        image: '/src/img/buy-comics-subscriptions.png',
                        label: 'SUBSCRIPTION'   
                    },
                    {
                        image: '/src/img/buy-comics-shop-locator.png',
                        label: 'COMIC SHOP LOCATOR'   
                    },
                    {
                        image: '/src/img/buy-dc-power-visa.svg',
                        label: 'DC POWER VISA', 
                        isSvg: true  
                    },
        
                ]
            }
        }
    }
</script>
<template>
    <div class="bg-blue">
        <div class="container">
            <a v-for="(image, index) in images" :key="index" href="">
                <img :src="image.image" :class="{ 'svg-img': image.isSvg } ">
                <span>{{ image.label }}</span>
            </a>
        </div>
    </div>
    <div class="bg-image">
        <div class="container">

        </div>
    </div>
    <div class="bg-grey">
        <div class="container">

        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    .bg-blue{
        background-color: $color;
        padding: 20px;
    }

    .bg-image{
        background-image: url(../img/footer-bg.jpg);
    }

    .bg-grey{
        background-color: #303030;
    }

    .container{
        max-width: 1070px;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
        img{
            width: calc(100% / 5 );
            vertical-align: middle;
        }
        a{
            text-decoration: none;
            color: #fff;
            font-size: 10px;
            span{
                margin-left: 10px;
            }
        }
        .svg-img {
            width: 60px; /* Imposta la larghezza desiderata per l'immagine SVG */
        }
    }
</style>