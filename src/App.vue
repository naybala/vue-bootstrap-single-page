<template>
  <Navbar />
  <ShowCase />
  <SignUp />
</template>

<script>
import Navbar from "./components/Navbar.vue";
import ShowCase from "./components/ShowCase.vue";
import SignUp from "./components/SignUp.vue";
export default {
  name: "App",
  components: {
    Navbar,
    ShowCase,
    SignUp,
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
