<script>
export default {
    name: "AppFooter",
    data(){
        return{
            content:[
                {
                    text: "DIGITAL COMICS",
                    img: "../assets/images/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    img: "",
                },
                {
                    text: "SUBSCRIPTION",
                    img: "",
                },
                {
                    text: "COMIC SHOP LOCATION",
                    img: "",
                },
                {
                    text: "DC POWER VISA",
                    img: "",
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
            ]

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
    <!-- bonus section -->
    <section id="bonus-section">
        <ul>
            <li v-for="link in content">
                <img :src="getImageURL(`link.img`)" alt="">
                {{ link.text }}
            </li>
        </ul>
    </section>
    <!-- info e useful links section  -->
    <section id="info-section">
        <div>
            <div style="display: flex;">
                <ul v-for="ul in footerUlContent">
                    <li>{{ ul.title }}</li>
                    <li v-for="cnt in ul.contents"> <a v-for="a in cnt" href="">{{ a }}</a></li>
                </ul>
 
            </div>

        </div>
    </section>
    <!-- media section  -->
    <section>
        
    </section>
</template>

<style lang="scss" scoped>

    #bonus-section{ 
        background-color: rgb(13,110,253);
        color: white;
        height: 150px;
        display: flex;
        justify-content: center;
        ul {
            display: flex;
            list-style-type: none;
            justify-content: center;
            align-items: center;
            
            li {
                font-weight: bold;
                padding-right: 30px;
            }
        }
    }
    #info-section {
        background-image: url("../assets/images/footer-bg.jpg");
        height: 300px;
        color: white;
        ul{
            list-style-type: none;
            a{
                color: grey;
                padding-left: 10px;
                text-decoration: none;
            }

        }

    }

</style>
