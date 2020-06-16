<template lang="html">
  <div>
    <input @keyup.enter="onInput" />
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  methods: {
    onInput() {
      this.$emit('searchTermChange', event.target.value);
    },
  },
};
</script>

<style lang="css" scoped>
input {
  width: 75%;
}
div {
  text-align: center;
  margin: 20px;
}
</style>
