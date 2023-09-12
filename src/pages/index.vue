<template>
  <div>
     <div>
<!--       Logo Section-->
       <logo />
<!--       Hero Section -->
       <Video/>
<!--       Channel Section -->
       <div class="container mx-auto grid  grid-cols-3  xl:grid-cols-5 2xl:grid-cols-7 py-16 gap-4 px-2 md:px-2">
         <div v-for="(channel, i) in channels" :key="i" class=" flex justify-center">
           <channel-card :channel="channel" :index="i" />
         </div>
       </div>

     </div>
  </div>
</template>

<script setup>
const channels = [
  { name: "Star Jalsha", image: "/channel/channel1.png" },
  { name: "BTV", image: "/channel/channel2.png" },
  { name: "Star Plus", image: "/channel/channel3.png" },
  { name: "Independent", image: "/channel/channel4.png" },
  { name: "Channel 9", image: "/channel/channel5.png" },
  { name: "T-Sports", image: "/channel/channel6.png" },
  { name: "Star Sports 2", image: "/channel/channel7.png" },
  { name: "Star Jalsha", image: "/channel/channel1.png" },
  { name: "BTV", image: "/channel/channel2.png" },
  { name: "Star Plus", image: "/channel/channel3.png" },
  { name: "Independent", image: "/channel/channel4.png" },
  { name: "Channel 9", image: "/channel/channel5.png" },
  { name: "T-Sports", image: "/channel/channel6.png" },
  { name: "Star Sports 2", image: "/channel/channel7.png" }
]
</script>

<style lang="scss" scoped>

</style>
