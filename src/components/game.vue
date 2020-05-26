<template>
  <div class="m-game">
    <div class="m-game_step-1" v-if="step === 1">
      <div class="m-game_group -two">
        <button class="m-game_action -paper" @click="play(1)"/>
        <button class="m-game_action -scissors" @click="play(2)"/>
      </div>
      <div class="m-game_group -one">
        <button class="m-game_action -rock" @click="play(3)"/>
      </div>
    </div>
    <div class="m-game_step-2" v-else-if="step === 2">
      <div class="m-game_choice">
        <span class="m-game_picked">You picked</span>
        <button class="m-game_action" v-bind:class="[choice, { '-win': win }]"/>
      </div>
      <div v-if="adversary">
        You lose
        <button>Play again</button>
      </div>
      <div class="m-game_choice">
        <span class="m-game_picked">The house picked</span>
        <button class="m-game_action" v-bind:class="[adversary, { '-win': lose }]"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'game',
  data() {
    return {
      step: 1,
      choice: null,
      adversary: null,
      choices: { 1: '-paper', 2: '-scissors', 3: '-rock' },
      win: false,
      lose: false,
    };
  },
  methods: {
    play(choice) {
      this.step = 2;
      this.choice = this.choices[choice];
      setTimeout(() => {
        this.adversary = this.choices[Math.floor(Math.random() * (2 + 1) + 1)];
      }, 2000);
    },
  },
};
</script>
