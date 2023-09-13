<template>
  <div class="w-full">
    <div class="relative">
      <div class="bg-white p-4 md:p-8 flex flex-col justify-between flex-grow-1 rounded-tr-2xl rounded-bl-2xl">
        <div class="flex  justify-center items-center py-6">
          <img class="h-[60px] md:h-[100px]" :src="channel.image"/>
        </div>
      </div>
      <div :class="index % 2 === 0 ? 'bottom-3' : 'top-3'" class="absolute   w-full left-0">
        <div :class="index % 2 === 0 ? 'rounded-tr-[36px]' : 'rounded-br-[36px]'"
             class="bg-gradient-to-r md:w-[80%] from-cyan-500 to-blue-500  py-1 md:py-2 px-2 md:px-6  text-[12px] md:text-[16px] text-white font-[600]">
          {{ channel.name }}
        </div>
      </div>
      <div :class="index % 2 !== 0 ? 'bottom-0' : 'top-0'" class="absolute  order-2 left-0 w-full">
        <img :class="index % 2 !== 0 ? 'rotate-180' : ''" class="h-[58px]  w-full  rounded-tr-2xl"
             src="/image/card.png"/>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  channel: {
    type: Object,
    default: {},
  },
  index: {type: String || Number, default: ''}
});
</script>

<style lang="scss" scoped>

</style>


<!--

-->