<template>
  <div class="card">
    <div v-for="q in questions" :key="q.id">
      <div v-if="complete">
        <h3 class="message">{{ $t("complete") }}</h3>
        <ul>
          <li>
            <a class="final-link" href="https://www.aka.ms/ICWebinarOct"
              >Webinar 1, "Advice from an Imagine Cup Competition Veteran with Dmitry Soshnikov" has already been completed. View the recording here!"<br></br></a
            >
          </li>
          <li>
            <a class="final-link" href="https://www.aka.ms/ICWebinarNov"
              >Live Webinar for November - Session Title: Capturing & Analyzing Data for Your Project<br></br></a
            >
          </li>
          <li>
            <a class="final-link" href="https://www.aka.ms/ICWebinarDec"
              >Live Webinar for December - Session Title: Serverless – What is it & how can I use it for my project<br></br></a
            >
          </li>
          <li>
            <a class="final-link" href="https://www.aka.ms/ICWebinarJan"
              >Live Webinar for January - Session Title: How to Prepare a Great Presentation</a
            >
          </li>
        </ul>
      </div>
      <div v-else>
        <h3 v-if="error" class="error">{{ $t("error") }}</h3>
        <h2>
          {{ q.quiz[currentQuestion].questionText }}
        </h2>
        <div>
          <button
            :key="index"
            v-for="(option, index) in q.quiz[currentQuestion].answerOptions"
            @click="handleAnswerClick(option.isCorrect)"
            class="btn ans-btn"
          >
            {{ option.answerText }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import messages from "@/assets/translations";

export default {
  name: "Quiz",
  data() {
    return {
      currentQuestion: 0,
      complete: false,
      error: false,
      route: "",
      locale: "",
    };
  },
  computed: {
    questions() {
      return this.$t("quizzes");
    },
  },

  i18n: { messages },
  methods: {
    handleAnswerClick(isCorrect) {
      this.error = false;
      let nextQuestion = this.currentQuestion + 1;
      if (isCorrect == "true") {
        //always 3 questions per quiz
        if (nextQuestion < 15) {
          this.currentQuestion = nextQuestion;
        } else {
          this.complete = true;
        }
      } else {
        this.error = true;
      }
    },
  },
};
</script>

<style scoped>
li {
  list-style-type: none;
}
</style>
