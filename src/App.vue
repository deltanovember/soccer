<template>
  <div id="app">
    <div class="sports-field">
      <h1>{{ title }}</h1>
      <goal></goal>
      <ball></ball>
    </div>
  </div>
</template>

<script>
import Ball from "./components/Ball.vue";
import Goal from "./components/Goal.vue";
export default {
  components: {
    Ball,
    Goal
  },
  data() {
    return {
      status: "",
      title: "Getting started",
      goalClass: "something-great"
    };
  },

  methods: {
    shoot() {
      const results = ["miss", "score"];

      this.status = results[Math.floor(Math.random() * results.length)];

      setTimeout(() => {
        this.reset();
      }, 800);
    },

    reset() {
      this.status = "reset";
      setTimeout(() => {
        this.status = "";
      }, 500);
    },

    imageSrc() {
      return "/static/soccer-goal.png";
    }
  }
};
</script>

<style>
</style>
