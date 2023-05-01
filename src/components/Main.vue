<script>
export default {
  name: "Main"
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

  </main>
</template>


<style long="scss" scoped>
  main{
    height: 150px;
    background-color:#1C1C1C;
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
          padding: 10px 25px;
          color: white;
          font-size: 27px;
          font-weight: 600;
          bottom: -25px;
          left: 18%;
        }


</style>