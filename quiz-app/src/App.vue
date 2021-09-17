<template>
  <div>
    <nav>
      <!--<label for="locale">locale</label>
      <select v-model="locale">
        <option>en</option>
      </select>-->
      <img src="@/assets/banner.png" alt="Imagine Cup Banner"/>
    </nav>
    <div id="app">
      <h1>{{ $t("title") }}</h1>
      
        <Quiz />
      
    </div>
  </div>
</template>

<script>
import Quiz from "@/components/Quiz.vue";
import messages from "@/assets/translations";

export default {
  name: "App",
  i18n: { messages },
  components: {
    Quiz,
  },
  data() {
    return {
      locale: "en",
    };
  },
  
};
</script>

<style>

body {
    margin: 0px;
}

html {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: black;
}
nav {
  background-color: black;
}

nav a {
  color: white;
  text-align: right;
}

.link {
  display: list-item;
}

h1,
h2,
h3,
.message {
  text-align: center;
}
.final-link {
  text-align: center;
  font-weight: bold;
}
.error {
  color: red;
}
.card {
  width: 60%;
  border: black solid;
  border-radius: 5px;
  margin: auto;
  padding: 1em;
  text-align: center;
  margin-bottom: 10px;
}
.btn {
  min-width: 50%;
  font-size: 20px;
  text-align: center;
  cursor: pointer;
  margin-bottom: 5px;
  width: 50%;
  color: #ffffff;
  background-color: #5C2C92;
  border-radius: 5px;
  padding: 5px;
  justify-content: flex-start;
  align-items: center;
}
.ans-btn {
  justify-content: center;
  display: flex;
  margin: 4px auto;
}
</style>
