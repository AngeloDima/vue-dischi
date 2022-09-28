<template>
    <div class="Midle">


        <div class="card-container">
            <div v-for="infoElementi in characters" :key="infoElementi.response">

                <div class="card">
                    <img :src="infoElementi.poster" alt="">
                    <p>{{infoElementi.title}}</p>
                    <p>{{infoElementi.author}}</p>
                    <p>{{infoElementi.year}}</p>
                </div>
                
            </div>
        </div>


    </div>
</template>

<script>
    export default {
  name: 'mainCode',
  props: {
    characters: Array
  }
}
</script>

<style lang="scss" scoped>
    .Midle{
        width: 100%;
        height: 80vh;
        background-color: #00ff84;
        display: flex;
        flex-wrap: wrap;
        align-content: space-around;
        justify-content: center;
        
        .card-container{
            width: 90%;
            height: 70vh;
            // background-color: rgba(255, 0, 0, 0.315);
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
            .card{
                width: 220px;
                height: 280px;
                background-color: aqua;
                display: flex;
                align-items: center;
                flex-direction: column;
                p{
                    margin: 8px 0px;
                    color: brown;
                    font-weight: 700;
                }
                img{
                    width: 150px;
                    height: 170px;
                    
                }
            }
        }
    }
    </style>