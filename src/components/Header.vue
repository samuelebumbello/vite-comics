<script>
import menuTop from "../js/menuTop.js";

export default {
    name: "Header",
    data(){
        return{
            menuTop,
        }
    }
}
</script>

<template>

  <header class="menu-header">
        <div class="dc-container">
                <img src="../assets/img/dc-logo.png" alt="">
            <div>
                <ul>
                    <li 
                    v-for="(menu, index) in menuTop"
                    :key="index">
                        <a href="">{{ menu.text }}</a>
                    </li>
                </ul>
            </div>
        </div>
  </header>

</template>

<style lang="scss">
    @import "../scss/general/variables";
    @import "../scss/general/general";

    header{
    display: flex;
    align-items: center;
    background-color:white;
    height: 120px;
    margin-top: 30px;
        img{
        width: 80px;
        };
   }

</style>