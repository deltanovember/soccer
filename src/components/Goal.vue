<template>
      <img
        :class="goalClass"
        class="soccer-goal"
        src="/static/soccer-goal.png"
        alt="Soccer goal">
</template>
<script>

    export default {
        data() {
            return {
                goalClass: "something"
            }
        }
    
    }
</script>