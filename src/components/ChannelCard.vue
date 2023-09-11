<template>
  <div class="w-full">
    <div class="bg-white flex flex-col justify-between flex-grow-1 rounded-tr-2xl rounded-bl-2xl relative">
      <div class="flex p-4 justify-center items-center">
        <img class="h-[100px]" :src="channel.image"/>
        <!--       <p>{{ channel.name }}</p>-->
      </div>
    </div>
    <div class="absolute top">
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