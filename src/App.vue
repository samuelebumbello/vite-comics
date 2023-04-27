<script>
// Facciamo l'import dei componenti che utilizzaremo all'interno del template
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  // All'interno di components dichiariamo sotto forma di proprietà l'import dei vari components.
  components:{
    Header,
    Main,
    Footer
  }
}

</script>

<template>
    <Header/>
    <Main/>
    <Footer/>
</template>

<style lang="scss" scoped>
  @use "./scss/main.scss" as *;
</style>
