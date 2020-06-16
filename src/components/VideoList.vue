<template lang="html">
  <ul class="list-group">
    <VideoListItem
      v-for="video in videoResults"
      :key="video.etag"
      :video="video"
      @videoSelection="onVideoSelect"
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
  methods: {
    onVideoSelect(video) {
      this.$emit('videoSelection', video);
    },
  },
};
</script>

<style lang="css" scoped></style>
