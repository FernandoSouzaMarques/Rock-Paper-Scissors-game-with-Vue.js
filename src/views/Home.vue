<template>
  <div class="home">
    <headerGame/>
    <game/>
    <rules/>
  </div>
</template>

<script>
// @ is an alias to /src
import headerGame from '@/components/header.vue';
import rules from '@/components/rules.vue';
import game from '@/components/game.vue';

export default {
  name: 'Home',
  components: { headerGame, rules, game },
};
</script>
