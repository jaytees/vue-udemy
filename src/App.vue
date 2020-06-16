<template lang="html">
  <div>
    <SearchBar @searchTermChange="onTermChange"></SearchBar>
  </div>
</template>

<script>
import SearchBar from './components/SearchBar';

export default {
  name: 'App',
  components: {
    SearchBar,
  },
  methods: {
    onTermChange(searchTerm) {
      console.log(searchTerm);
    },
  },
};
</script>

<style lang="css" scoped></style>
