<template>
 <v-app>
   <Home>
   </Home>
   <Works></Works>
   <Main></Main>
   <Footer></Footer>
 </v-app>
</template>

<script>
import Home from "./views/Home.vue";
import Footer from "./views/Footer.vue";
import Works from "./views/Works.vue";
import Main from "./views/Main.vue";

export default {
 name: "App",
 components: {
   Home,
   Footer,
   Works,
   Main,
 },
};
</script>
