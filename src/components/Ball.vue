<template>   
      <img
        class="soccer-ball"
        :class="status"
        src="/static/soccer-ball.png"
        alt="Soccer ball"
        @click="shoot">
</template>

<script>
export default {
  data() {
    return {
      status: ""
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
    }
  }
};
</script>