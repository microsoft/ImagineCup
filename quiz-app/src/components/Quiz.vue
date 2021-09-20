<template>
  <div class="card">
    <div v-for="q in questions" :key="q.id">
      <h3 v-if="complete" class="message">{{ $t("complete") }}</h3>
      <ul>
        <li><a class="final-link" href="https://www.aka.ms/ICVoucher" v-if="complete"
        >https://www.aka.ms/ICVoucher</a
      ></li>
      <li><a class="final-link" href="https://www.aka.ms/ICWebinarOct" v-if="complete"
        >Live Webinar for October</a
      ></li>
      <li><a class="final-link" href="https://www.aka.ms/ICWebinarNov" v-if="complete"
        >Live Webinar for November</a
      ></li>
      <li><a class="final-link" href="https://www.aka.ms/ICWebinarDec" v-if="complete"
        >Live Webinar for December</a
      ></li>
      <li><a class="final-link" href="https://www.aka.ms/ICWebinarJan" v-if="complete"
        >Live Webinar for January</a
      ></li>

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
