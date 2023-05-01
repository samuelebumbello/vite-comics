<script>
import jsonCard from "../data/dc-comics.json"

export default {
  name: "Main",
  props:{
    img: String,
    title: String
  },

  data() {
    return{
      jsonCard
    }
}
}
</script>

<template>
  <jumbotron>
    <!-- <img src="../assets/img/jumbotron.jpg" alt=""> -->
    <div class="jumbo-button">
      <div class="current-series">
        CURRENT SERIES
      </div>
    </div>
  </jumbotron>

  <main>

      <div class="cards-container">
        <div class="card" v-for="(element, index) in jsonCard" :key="index">
          <img :src="element.thumb" alt="">
          <span class="uppercase">{{ element.series }}</span>
        </div>
  
        <div class="load-more">
            <span>LOAD MORE</span>
        </div>
      </div>


  </main>
</template>


<style long="scss" scoped>
  main{
    height: 700px;
    background-color:#1C1C1C;
    display: flex;
    justify-content: center;
    padding-bottom: 18px;
  }

  jumbotron{
    background-image: url(../assets/img/jumbotron.jpg);
    height: 400px;
    display: inherit;
    position: relative;
  }

  .current-series{
    position: absolute;
    background-color: #0282F9;
    padding: 10px 30px;
    color: white;
    font-size: 27px;
    font-weight: 600;
    bottom: -25px;
    left: 16.5%;
  }

  .cards-container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 70%;
  }

  .card{
    height: 230px;
    width: 180px;
    color: white;
    margin: 50px 16px;
  }

  img{
    height: 180px;
    width: 180px;
    margin-bottom: 10px;
    object-fit: cover;
  }

  .load-more{
    background-color: #0282F9;
    color:white;
    font-size: 15px;
    padding: 5px 50px;
    margin-bottom:5px ;
    font-weight: 600;
    cursor: pointer;
  }

  .uppercase{
    text-transform: uppercase;
  }


</style>