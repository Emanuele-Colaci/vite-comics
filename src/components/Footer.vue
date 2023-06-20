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
        <div class="container1 content1">
            <a v-for="(image, index) in images" :key="index" href="">
                <img :src="image.image" :class="{ 'svg-img': image.isSvg } ">
                <span>{{ image.label }}</span>
            </a>
        </div>
    </div>
    <div class="bg-image">
        <div class="container2 row">
            <div class="col">
                <div class="d-flex">
                    <div>
                        <h2>DC COMICS</h2>
                        <p><a href="#">Characteres</a></p>
                        <p><a href="#">Comics</a></p>
                        <p><a href="#">Movies</a></p>
                        <p><a href="#">Tv</a></p>
                        <p><a href="#">Games</a></p>
                        <p><a href="#">Videos</a></p>
                        <p><a href="#">News</a></p>
                        <h2>SHOP</h2>
                        <p><a href="#">Shop DC</a></p>
                        <p><a href="#">Shop DC Collectibles</a></p>
                    </div>
                    <div class="margin-left">
                        <h2>DC</h2>
                        <p><a href="#">Terms Of Use</a></p>
                        <p><a href="#">Privacy policy (New)</a></p>
                        <p><a href="#">Ad Choices</a></p>
                        <p><a href="#">Advertising</a></p>
                        <p><a href="#">Jobs</a></p>
                        <p><a href="#">Subscriptions</a></p>
                        <p><a href="#">Talent Workshops</a></p>
                        <p><a href="#">CPSC Certificates</a></p>
                        <p><a href="#">Ratings</a></p>
                        <p><a href="#">Shop Help</a></p>
                        <p><a href="#">Contact Us</a></p>
                    </div>
                    <div class="margin-left">
                        <h2>SITES</h2>
                        <p><a href="#">DC</a></p>
                        <p><a href="#">MAD Magazine</a></p>
                        <p><a href="#">DC Kids</a></p>
                        <p><a href="#">DC Universe</a></p>
                        <p><a href="#">DC Power Visa</a></p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="image-container">
                    <img src="../img/dc-logo-bg.png" alt="logo-bg">
                </div>
            </div>
        </div>
    </div>
    <div class="bg-grey">
        <div class="container3 content3">
            <div>
                <button>SING-UP NOW!</button>
            </div>
            <div>
                <h3>FOLLOW US</h3>
                <div class="vertical">
                    <img src="../img/footer-facebook.png" alt="facebook">
                    <img src="../img/footer-twitter.png" alt="twitter">
                    <img src="../img/footer-youtube.png" alt="you-tube">
                    <img src="../img/footer-pinterest.png" alt="pintarest">
                    <img src="../img/footer-periscope.png" alt="periscope">
                </div>
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

    .bg-image{
        background-image: url(../img/footer-bg.jpg);
    }

    .bg-grey{
        background-color: #303030;
    }

    .container1, .container2, .container3{
        max-width: 1070px;
        margin: 0 auto;
    }
    .content1{
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
    .row{
        display: flex;
        justify-content: space-between;
        .col{
            h2{
                color: #fff;
                font-size: 17px;
                margin: 20px 0 5px 0;
            }
            a{
                color: grey;
                text-decoration: none;
                font-size: 13px;
            }
            .d-flex{
                display: flex;
                .margin-left{
                    margin-left: 40px;
                }
            }
        }
        .image-container {
            width: 100%;
            height: 21rem;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            object-fit: contain;
            object-fit: cover;
            img{
                width: 70%;
            }
        } 
    }
    .content3{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px 0;
        button{
            padding: 10px;
            border: 2px solid $color;
            background: none;
            color: #fff;
        }
        h3{
            display: inline-block;
            vertical-align: middle;
            margin-right: 10px;
            color: $color;
        }
        .vertical{
            vertical-align: middle;
            display: inline-block;
            img{
                margin-left: 10px;
            }
        }
    }
</style>