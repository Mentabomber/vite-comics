<script>
export default {
    name: "AppMain"
      
     
}

</script>

<template>
    <main>
        <div class="container">
            <!-- jumbotron  -->
            <div id="jumbotron">

            </div>

            <!-- comics selection menu  -->
        </div>
       
    </main>
</template>

<style lang="scss" scoped>
    main{
        height: 100px;
        width: 100%;
        background-color: black;
        .container {
            max-width: 1180px; margin: auto;
        }

        h1{
            color: white;
        }
        #jumbotron{
            background-image: url("..assets/images/jumbotron.jpg");
            height: 300px;
        }
    }
</style>
