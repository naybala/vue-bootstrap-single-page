<template>
  <div v-if="loading">
    <Loader />
  </div>
  <div v-if="!loading">
    <Navbar />
    <ScrollTop />
    <ShowCase />
    <SignUp />
    <Box />
    <LearnBase />
    <LearnFrameWork />
    <LearnDatabase />
    <Question />
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
import LearnBase from "./components/LearnBase.vue";
import LearnFrameWork from "./components/LearnFrameWork.vue";
import LearnDatabase from "./components/LearnDatabase.vue";
import Question from "./components/Question.vue";
import ScrollTop from "./components/ScrollTop.vue";
export default {
  name: "App",
  components: {
    Loader,
    Navbar,
    ShowCase,
    SignUp,
    Box,
    LearnBase,
    LearnFrameWork,
    LearnDatabase,
    Footer,
    Question,
    ScrollTop,
  },
  data: () => ({
    loading: true,
  }),
  mounted() {
    setTimeout(() => {
      document.querySelector(".loader").classList.add("fade-out");
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

@media (min-width: 290px) and (max-width: 500px) {
  .section {
    padding: 0rem;
  }
  .lead {
    font-size: 1rem;
  }
  p {
    font-size: 0.9rem;
  }
}
</style>
