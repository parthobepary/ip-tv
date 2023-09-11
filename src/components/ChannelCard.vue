<template>
  <div class="w-full">
    <div class="bg-white p-4 md:p-8 flex flex-col justify-between flex-grow-1 rounded-tr-2xl rounded-bl-2xl relative">
      <div class="flex  pb-4 md:pb-10 justify-center items-start">
        <img class="h-[60px] md:h-[100px]" :src="channel.image"/>
      </div>
    </div>
    <div class="absolute bottom-0 md:-bottom-4 bg-gradient-to-r from-cyan-500 to-blue-500  py-2 px-6 rounded-tr-[36px] text-white font-[600]">
      {{ channel.name }}
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  channel: {
    type: Object,
    default: {},
  },
});
</script>

<style lang="scss" scoped>

</style>