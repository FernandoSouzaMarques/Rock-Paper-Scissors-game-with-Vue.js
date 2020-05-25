<template>
  <div class="m-header">
    <div class="m-header_game">
      Rock<br>
      Paper<br>
      Scissors<br>
    </div>
    <div class="m-header_score">
      Score
      <strong class="score">{{score}}</strong>
    </div>
  </div>
</template>

<script>
export default {
  name: 'headerGame',
  data() {
    return {
      score: 12,
    };
  },
};
</script>
