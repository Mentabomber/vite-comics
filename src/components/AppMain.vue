<script>
import AppMainCards from './AppMainCards.vue';

export default {
    name: "AppMain",
    components: {
        AppMainCards

    },
    data(){
        return{
            products: [
            {
                "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book"
            },
            {
                "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book"
            },
            {
                "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel"
            },
            {
                "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book"
            },
            {
                "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book"
            },
            {
                "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel"
            }
            ]
        }
    }
      
     
}

</script>

<template>
    <main>
        
        <!-- jumbotron  -->
        <section id="jumbotron-section">
            <div class="container">
            
            </div>
        </section>
        <!-- comics selection menu  -->
       <section id="comics-menu-section">
            <div class="container">
                <div id="comics-menu">
                    <AppMainCards v-for="(product, index) in products" :key="index"
                    :details="product"
                    />
                    <div id="box-absolute">
            <h2>CURRENT SERIES</h2>
        </div>
                </div>
                <div id="button-box">
                    <button>
                    Load More
                    </button>
                </div>

            </div>
       </section>
            
    </main>
</template>

<style lang="scss" scoped>

    main{
        
        #box-absolute{
            position: absolute;
            left: 0px;
            top: -25px;
            background-color: blue;
            padding: 10px;
            max-width: 300px;
        }

        
        .container {
            max-width: 1180px; margin: auto;
        }

        h1{
            color: white;
        }
        #jumbotron-section{
            width: 100%;
            height: 300px;
            background-image: url("../public/images/jumbotron.jpg");
            background-size: cover;
        }
        #comics-menu{
            position: relative;
            padding: 20px;
            padding-top: 40px;
            display: flex;
            flex-wrap: wrap;
            color: white;
        }

        #comics-menu-section{
            background-color: black;
            width: 100%;

            img{
                width: 100%;
                height: 100%;
            }
        }
        #button-box{
            padding: 20px;
            text-align: center;
            button{
                color: white;
                background-color: rgb(13,110,253);
                padding: 10px 55px;
                border-radius: 5px;
                border: none;
            }
        }
    }

    
</style>
