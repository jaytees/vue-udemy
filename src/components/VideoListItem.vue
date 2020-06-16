<template lang="html">
  <li class="list-group-item media" @click="onVideoSelect">
    <img class="mr-3" :src="thumbnailUrl" alt="" />
    <div class="media-body">
      <p>{{ video.snippet.title }}</p>
    </div>
  </li>
</template>

<script>
export default {
  name: 'videoListItem',
  props: {
    video: Object,
  },
  computed: {
    thumbnailUrl() {
      return this.video.snippet.thumbnails.default.url;
    },
  },
  methods: {
    onVideoSelect() {
      this.$emit('videoSelection', this.video);
    },
  },
};
</script>

<style lang="css" scoped>
li {
  display: flex;
  cursor: pointer;
}
li:hover {
  background-color: #eee;
}
</style>
