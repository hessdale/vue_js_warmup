<template>
  <div>
    <button @click="change_back">Change Background</button>
    <section v-for="(secret, i) in secrets" :key="i">
      <p @click="change_pink">{{ secret }}</p>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    change_back: function () {
      document.body[`style`][`background`] = `blue`;
    },
    change_pink(details) {
      details[`target`][`style`][`color`] = `pink`;
    },
  },
  data() {
    return {
      secrets: [`secret1`, `secret2`, `secret3`, `secret4`, `secret5`],
    };
  },
};
</script>

<style scoped>
</style>