<template>
  <p>Reaction Time - {{ scoreRes }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>
<script>
export default {
  props: ["scoreRes"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.scoreRes < 250) {
      this.rank = "Fast Fingers";
    } else if (this.scoreRes < 400) {
      this.rank = "Rapid Reflexes";
    } else {
      this.rank = "Slow One...";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
