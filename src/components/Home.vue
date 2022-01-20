<template>
  <div class="main">
    <div class="container">
      Day <br /><span>{{ df }}</span>
    </div>
  </div>
</template>

<script>
import moment from "moment";

export default {
  name: "Home",
  props: {
    msg: String,
  },
  data() {
    return {
      df: moment().diff(moment("20220116", "YYYYMMDD"), "days"),
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;900&display=swap');

* {
  margin: 0;
  padding: 0;
}
.main {
  margin: 0;
  padding: 0;
  background:linear-gradient(rgba(0, 0, 0, 0.5),rgba(0, 0, 0, 0.5)), url("./../assets/bg.jpg") #0b181e;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
.container {
  font-family: "Roboto", sans-serif;
  text-align: center;
  font-weight: lighter;
  color: white;
  font-size: 3rem;
  text-transform: uppercase;
  font-weight: 100;
}
.container span {
  font-weight: 900;
  font-size: 5rem;
  font-style: normal;
}
</style>
