<script>


export default {
    name: "AppFooter",
    data(){
        return{
            content:[
                {
                    text: "DIGITAL COMICS",
                    img: "images/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    img: "images/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    img: "images/buy-comics-subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATION",
                    img: "images/buy-comics-shop-locator.png",
                },
                {
                    text: "DC POWER VISA",
                    img: "images/buy-dc-power-visa.svg",
                },
            ],
            footerUlContent: [
                {
                    title: "DC COMICS",
                    contents: ["Characters", "Comics","Movies","TV","Games","Videos","News"]
                },
                {
                    title: "SHOP",
                    contents: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "DC",
                    contents: ["Terms Of Use", "Privacy policy(New)","Ad Choices","Advertising","Jobs","Subscriptions","Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
                },
                {
                    title: "SITES",
                    contents: ["DC", "MAD Magazine","DC Kids","DC Universe","DC Power Visa"]
                }
            ],
            mediaImages: ["images/footer-facebook.png", "images/footer-twitter.png", "images/footer-youtube.png", "images/footer-pinterest.png", "images/footer-periscope.png"]

        }
    },
    methods: { 
        getImageURL: function(imgPath){
            return new URL (imgPath, import.meta.url).href;
        }
    }
      
     
}

</script>

<template>
    <footer>
        
            <!-- bonus section -->
            <section id="bonus-section">
                <div class="container">
                    <ul>
                        <li v-for="link in content">
                            <img :src="link.img" alt="">
                            <span>{{ link.text }}</span>
                            
                        </li>
                    </ul>
                </div>
            </section>
            <!-- info e useful links section  -->
            <section id="info-section">
                <div class="container">
                    <div style="display: flex; justify-content: space-between; ">
                        <div style="display: flex;  padding-right: 10px; position: relative; z-index: 1001;"> 

                            <ul v-for="ul in footerUlContent">
                                <li>{{ ul.title }}</li>
                                <li v-for="cnt in ul.contents"> <a href="">{{ cnt }}</a></li>
                            </ul>
            
                        </div>
                        <div class="img-container">
                            <img id="background-img"  :src="getImageURL(`../public/images/dc-logo-bg.png`)" alt="logo-dc-bg">
                        </div>
                    </div>
                </div>
            </section>
            <!-- media section  -->
            <section id="media-section">
                <div class="container">
                    <button>
                        SIGN-UP NOW!
                    </button>
                    <div>
                    
                        <ul>
                            <li> <span>
                            FOLLOW US
                        </span></li>
                            <li v-for="img in mediaImages">
                                <a href=""><img :src="img" alt=""></a>
                            </li>
                        </ul>
                    </div>
                </div>
            </section>
       
    </footer>
</template>

<style lang="scss" scoped>

    footer{
        position: relative;
        .container {
            max-width: 1180px; margin: auto;
        }
        #bonus-section{ 
            position: relative;
            z-index: 998;
            background-color: rgb(13,110,253);
            color: white;
            width: 100%;
            height: 150px;
            display: flex;
            justify-content: center;
            ul {
                display: flex;
                list-style-type: none;
                justify-content: center;
                align-items: center;
                
                li {
                    display: flex;
                    align-items: center;
                    font-weight: bold;
                    padding-right: 30px;
                }
            }
            img{
                width: 50px;
                height: 50px;
                margin-right: 10px;
                
            }
        }
        #info-section {

            padding: 40px 0;
            background-image: url("../public/images/footer-bg.jpg");

            background-size: cover;
            height: 300px;
            color: white;
    
                    ul{
                        list-style-type: none;
                        padding-right: 15px;

                        a{
                            color: grey;
                            
                            text-decoration: none;
                        }
    
            }
    
        }
        .img-container{
            max-height: 300px;
            width: 300px;
            img {
            height: 100%;
            width: 100%;
            object-fit: contain;
        }
        }
        #media-section{
            position: relative;
            z-index: 999;
            button{
                height: 50%;
                border: 2px solid rgb(13,110,253);
                background-color: rgb(36,41,47);
                color: white;
                padding: 5px;
            }
            div.container {
                display: flex;
                justify-content: space-between;
                align-items: center;
                height: 100%;
            }
            div{
                span{
                    color:rgb(13,110,253);
                    font-size: 20px;
                    font-weight: bold;
                }
            }
            height: 100px;
            background-color: rgb(36,41,47);
            ul{
    
                        display: flex;
                        align-items: center;
                        list-style-type: none;
                        li{
                            padding-right: 15px;
                        }
                        a{
                            color: grey;
                            padding-left: 10px;
                            text-decoration: none;
                        }
    
            }
        }
    }
    #background-img{
        position: absolute;
        bottom: 0;
        right: 0;
        z-index: 1;
        padding-left: 50%;
    }
    

</style>
