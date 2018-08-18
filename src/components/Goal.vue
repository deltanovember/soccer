<template>
      <img
        :class="goalClass"
        class="soccer-goal"
        :src="imageSrc()"
        alt="Soccer goal">
</template>
<script>
export default {
  data() {
    return {
      goalClass: "something"
    };
  },

  methods: {
    imageSrc() {
      return "/static/soccer-goal.png";
    }
  }
};
</script>