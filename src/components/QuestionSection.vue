<template>
  <div>
    <likert-question
      v-for="item in questionItems"
      v-bind:key="item.id"
      v-bind:questionNo="item.id"
      v-bind:questionText="item.questionText"
      v-bind:minDegreeText="item.minDegreeText"
      v-bind:maxDegreeText="item.maxDegreeText"
      v-bind:scaleRange="item.scaleRange"
    ></likert-question>

    <choice-question
        v-for="item in choiceItems"
      v-bind:key="item.id"
      v-bind:questionNo="item.id+10"
      v-bind:questionText="item.questionText"
      v-bind:choice1 = "item.choice1"
      v-bind:choice2 = "item.choice2"
      v-bind:choice3 = "item.choice3"
      ></choice-question>
  </div>
</template>
<script>
import LikertQuestion from "./questionnaire/LikertQuestion.vue";
import ChoiceQuestion from "./questionnaire/ChoiceQuestion.vue";
export default {
  components: {
    LikertQuestion,
    ChoiceQuestion,
  },
  data: function() {
    return {
      questionItems: [
        {id: 1, questionText : "New ideas and projects sometimes distract me from previous ones.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 2, questionText : "Setbacks don’t discourage me. I don’t give up easily.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 3, questionText : "I often set a goal but later choose to pursue a different one.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 4, questionText : "I am a hard worker.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 5, questionText : "I have difficulty maintaining my focus on projects that take more than a few months to complete.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 6, questionText : "I finish whatever I begin.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 7, questionText : "My interests change from year to year.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 8, questionText : "I am diligent. I never give up.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 9, questionText : "I have been obsessed with a certain idea or project for a short time but later lost interest.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
        {id: 10, questionText : "I have overcome setbacks to conquer an important challenge.", minDegreeText : "Not like me at all", maxDegreeText : "Very much like me", scaleRange : "5"},
      ],
      choiceItems: [
          {id: 1, questionText : "First Moo" , choice1 : "Max", choice2 : "Average" ,choice3 : "Min" },
          {id: 2, questionText : "First Moo" , choice1 : "Max", choice2 : "Average" ,choice3 : "Min" },
          {id: 3, questionText : "First Moo" , choice1 : "Max", choice2 : "Average" ,choice3 : "Min" }
      ]
    };
  }
}
</script>