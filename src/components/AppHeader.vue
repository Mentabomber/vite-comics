<script>
export default {
    name: "AppHeader",
    data(){
        return {
            links: [
                {
                   text: "CHARACTERS",
                   url: "#",
                   current: false 
                },
                {
                   text: "COMICS",
                   url: "#",
                   current: true
                },
                {
                   text: "MOVIES",
                   url: "#",
                   current: false 
                },
                {
                   text: "TV",
                   url: "#",
                   current: false 
                },
                {
                   text: "GAMES",
                   url: "#",
                   current: false 
                },
                {
                   text: "COLLECTIBLES",
                   url: "#",
                   current: false 
                },
                {
                   text: "VIDEOS",
                   url: "#",
                   current: false 
                },
                {
                   text: "FANS",
                   url: "#",
                   current: false 
                },
                {
                   text: "NEWS",
                   url: "#",
                   current: false 
                },
                {
                   text: "SHOP",
                   url: "#",
                   current: false 
                },
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
    <header>
        <nav class="container">
            <!-- div logo -->
            <div>
                <img src="images/dc-logo.png" alt="logo-dc">
            </div>

            <!-- div lista navbar -->
            <div>
            
                <ul>
                    <li v-for="(link, i) in links"  :key="i">
                        <a :class="link.current ? 'active' : ''" :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>

    header{
        .container {
            max-width: 1180px; margin: auto;
        }
        nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 150px;
    }
    }


    div {
        ul {
            display: flex;
            list-style-type: none;
            align-items: center;
            padding-top: 11%;   
            // padding top cosi e anche padding bottom 50px nei li per far stare il bordo sotto al confine con il main
            
            li {
                padding-right: 10px;
                padding-bottom: 50px;
                font-weight: bold;
                color: black;
                &.active,
                &:hover{
                    color: rgb(13,110,253);
                    
                                  }
                a{
                    text-decoration: none;
                    &.active,
                    &:hover{
                    color: rgb(13,110,253);
                    border-bottom: 4px solid rgb(13,110,253);
                    padding-bottom: 50px;}
                }

            }
        }
    }
    

</style>
