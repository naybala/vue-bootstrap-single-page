<template>
  <div v-if="loading">
    <Loader />
  </div>
  <div v-if="!loading">
    <Navbar />
    <ShowCase />
    <SignUp />
    <Box />
    <Footer />
  </div>
</template>

<script>
import Loader from "./components/Loader.vue";
import Navbar from "./components/Navbar.vue";
import ShowCase from "./components/ShowCase.vue";
import SignUp from "./components/SignUp.vue";
import Box from "./components/Box.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Loader,
    Navbar,
    ShowCase,
    SignUp,
    Box,
    Footer,
  },
  data: () => ({
    loading: true,
  }),
  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 3000);
  },
};
</script>

<style>
body::before {
  display: block;
  content: "";
  height: 60px;
}
/* 
#map {
  width: 100%;
  height: 100%;
  border-radius: 10px;
} */

@media (min-width: 768px) {
  .news-input {
    width: 50%;
  }
}

@media (min-width: 576px) {
  .footer {
    padding: 0;
  }
}
</style>
