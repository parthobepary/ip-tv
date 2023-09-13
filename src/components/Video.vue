
<template>
  <div>
    <video id="video-player" controls muted
      class="cld-video-player cld-fluid vjs-live cld-video-player-skin-dark md:w-2/3 h-96 mx-auto" />
    <p class=" text-gray-800 text-sm text-center"> </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cld: null,
      video: 'samples/cld-sample-video'
    };
  },

  mounted() {
    this.cld = cloudinary.Cloudinary.new({ cloud_name: 'diqviipio' });
    let demoplayer = this.cld.videoPlayer(
      'video-player',
      {
        autoplay: true,
        loop: true
      }
    )
      .width(600);
    demoplayer.source(this.video);

    var liveControls = document.getElementsByClassName("vjs-live-control");

    demoplayer.on("play", function () {
      liveControls[0].classList.remove("vjs-hidden");

      demoplayer.currentTime(
        parseInt((new Date).getSeconds() % demoplayer.duration())
      );
    });
  },

}
</script>

<style>
body {
  font-family: sans-serif;
}

.cld-video-player .vjs-control-bar .vjs-progress-control {
  display: none;
}

div.vjs-control-bar>div.vjs-live-control.vjs-control {
  display: block;
}
</style>