<template lang="html">
  <li class="list-group-item">
    {{ video.snippet.title }}
  </li>
</template>

<script>
export default {
  name: 'videoListItem',
  props: {
    video: Object,
  },
};
</script>

<style lang="css" scoped></style>
