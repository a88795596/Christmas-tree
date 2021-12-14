<template>
  <div>
    <video autoplay loop :src="require('@/assets/video.mp4')" />
    <audio style="display: none" autoplay :src="require('@/assets/music.mp3')"></audio>
  </div>
</template>

<script>
export default {
  name: "landing-page",
  methods: {
    open(link) {
      this.$electron.shell.openExternal(link);
    },
  },
  created() {},
};
</script>

<style>
video {
  width: 100vw;
  height: 100vh;
}
</style>
