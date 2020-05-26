<template>
  <div class="m-rules">
    <div v-if="rules">
      <div class="m-rules_overlay" @click="rules = !rules"/>
      <div class="m-rules_modal">
        <div class="m-rules_modal-header">
          <h2 class="m-rules_modal-title">Rules</h2>
          <button class="m-rules_modal-close" @click="rules = !rules"/>
        </div>
        <div class="m-rules_modal-content">
          <img src="@/assets/image-rules.svg" alt="">
        </div>
      </div>
    </div>
    <button class="m-rules_button" @click="rules = !rules">Rules</button>
  </div>
</template>

<script>
export default {
  name: 'rules',
  data() {
    return {
      rules: false,
    };
  },
};
</script>
