<script>
import { dcComics, sites, shop, dc } from '../js/listFoot.js';

export default {
  name: "Footer",
  data(){
    return{
      dcComics,
      sites,
      shop,
      dc
    }
  }
}

</script>

<template>
  <div class="footer-top">

      <ul>
        <li>
          <img src="../assets/img/buy-comics-digital-comics.png" alt="">
          <span>DIGITAL COMICS</span>
        </li>
      </ul>
      <ul>
        <li>
          <img src="../assets/img/buy-comics-merchandise.png" alt="">
          <span>DIGITAL COMICS</span>
        </li>
      </ul>
      <ul>
        <li>
          <img src="../assets/img/buy-comics-subscriptions.png" alt="">
          <span>DIGITAL COMICS</span>
        </li>
      </ul>
      <ul>
        <li>
          <img src="../assets/img/buy-comics-shop-locator.png" alt="">
          <span>DIGITAL COMICS</span>
        </li>
      </ul>
      <ul>
        <li>
          <img class="img-svg" src="../assets/img/buy-dc-power-visa.svg" alt="">
          <span>DIGITAL COMICS</span>
        </li>
      </ul>


</div>
  <footer>
    <div class="dc-container">


      <div class="footer-left-menu">

        <div class="dc-me">
          <div>
            <h4>DC COMICS</h4>
            <ul>
              <li
              v-for="(comics, index) in dcComics"
              :key="index">
                <a href="">{{ comics.text }}</a>
              </li>
            </ul>
          </div>

          <div class="dc-mt">

            <h4>SHOP</h4>
            <ul>
              <li
              v-for="(merch, index) in shop"
              :key="index">
                  <a href="">{{ merch.text }}</a>
              </li>
            </ul>
          </div>
        </div>

        <div class="dc-me">
          <h4>DC</h4>
          <ul>
            <li
            v-for="(dc, index) in dc"
            :key="index">
              <a href="">{{ dc.text }}</a>
            </li>
          </ul>
        </div>

        <div>
          <h4>SITES</h4>
          <ul>
            <li
              v-for="(site, index) in sites"
              :key="index">
                  <a href="">{{ site.text }}</a>
              </li>
          </ul>
        </div>

        
      </div>
    </div>
    <img src="../assets/img/dc-logo-bg.png" alt="">
    
  </footer>

  <div class="footer-bottom">
    <div class="dc-container">
      <button>SIGN-UP NOW!</button>
      <div class="follow-us-flex">

        <h4>FOLLOW US</h4>
        <img src="../assets/img/footer-facebook.png" alt="">
        <img src="../assets/img/footer-youtube.png" alt="">
        <img src="../assets/img/footer-twitter.png" alt="">
        <img src="../assets/img/footer-pinterest.png" alt="">
        <img src="../assets/img/footer-periscope.png" alt="">
        
        
      </div>
    </div>
    

  </div>
</template>

<style lang="scss" scoped>
@import "../scss/general/general";
@import "../scss/general/variables";

footer{
  display: flex;
  align-items: center;
  min-height: 350px;
  height: 150px;
  position: relative;
  overflow: hidden;
  background-image: url(../assets/img/footer-bg.jpg);
  background-size: cover;
    img{
      position: absolute;
      right: 300px;
      
  }
}

.footer-top{
  display: flex;
  align-items: center;
  justify-content: center;
  height: 150px;
  background-color: #0282F9;
    img{
      margin-right: 15px;
    }
}

.footer-top ul li{
  display: flex;
  align-items: center;
  list-style: none;
    span{
      vertical-align: middle;
      color: white;
    }
    img{
      height: 50px;
      &.img-svg{
        width: 60px;
      }
    }
}

.footer-bottom{
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #373737;
  width: 100%;
  height: 110px;
      button{
        font-size: 15px;
        font-weight: bold;
        padding: 15px;
        border: 2px solid #0C7CEC;
        color: white;
        background-color: rgba(255, 255, 255, 0);
      }
      .follow-us-flex{
        display: flex;   
        align-items: center;
        h4{
          font-size: 20px;
          margin-right: 10px;
          color: #0C7CEC;
        }
        img{
          margin-left: 20px;
        }
      }
   
}

</style>