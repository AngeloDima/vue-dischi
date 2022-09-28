<template>
    <div class="Midle">


        <div class="card-container">
            <div v-for="infoElementi in characters" :key="infoElementi.response">

                <div class="card">
                    <img :src="infoElementi.poster" alt="">
                    <h2>{{infoElementi.title}}</h2>
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
        height: 90vh;
        background-color: #1e2d3b;
        display: flex;
        flex-wrap: wrap;
        align-content: space-around;
        justify-content: center;
        
        .card-container{
            width: 90%;
            height: 80%;
            // background-color: rgba(255, 0, 0, 0.315);
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 80px;
            .card{
                width: 220px;
                height: 300px;
                 background-color: #2e3a46;
                display: flex;
                align-items: center;
                flex-direction: column;
                h2{
                    color: white;
                    text-align: center;
                }
                p{
                    margin: 8px 0px;
                    color: brown;
                    font-weight: 700;
                    text-align: center;
                }
                img{
                    width: 150px;
                    height: 170px;
                    
                }
            }
        }
    }
    </style>