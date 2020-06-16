<template lang="html">
  <ul>
    <VideoListItem
      v-for="video in videoResults"
      :key="video.id.videoId"
      v-bind:video="video"
    ></VideoListItem>
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
