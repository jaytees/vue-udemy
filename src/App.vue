<template lang="html">
  <div>
    <SearchBar @searchTermChange="onTermChange"></SearchBar>
  </div>
</template>

<script>
import axios from 'axios';
import SearchBar from './components/SearchBar';

export default {
  name: 'App',
  components: {
    SearchBar,
  },
  methods: {
    onTermChange(searchTerm) {
      axios
        .get('https://www.googleapis.com/youtube/v3/search', {
          params: {
            key: process.env.VUE_APP_API_KEY,
            type: 'video',
            part: 'snippet',
            q: searchTerm,
          },
        })
        .then(res => console.log(res));
    },
  },
};
</script>

<style lang="css" scoped></style>
