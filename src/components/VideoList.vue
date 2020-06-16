<template lang="html">
  <ul>
    <VideoListItem></VideoListItem>
  </ul>
</template>

<script>
import VideoListItem from './VideoListItem';

export default {
  name: 'VideoList',
  components: {
    VideoListItem,
  },
  props: {
    videoResults: Array,
  },
};
</script>

<style lang="css" scoped></style>
