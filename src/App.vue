<template>
  <Navbar />
  <ShowCase />
  <SignUp />
  <Box />
  <Footer />
</template>

<script>
import Navbar from "./components/Navbar.vue";
import ShowCase from "./components/ShowCase.vue";
import SignUp from "./components/SignUp.vue";
import Box from "./components/Box.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Navbar,
    ShowCase,
    SignUp,
    Box,
    Footer,
  },
};
</script>

<style>
body::before {
  display: block;
  content: "";
  height: 60px;
}

#map {
  width: 100%;
  height: 100%;
  border-radius: 10px;
}

@media (min-width: 768px) {
  .news-input {
    width: 50%;
  }
}
</style>
