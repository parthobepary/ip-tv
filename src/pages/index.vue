<template>
  <div class="container mx-auto ">
    <div>
      <!--       Logo Section-->
      <logo />
      <!--       Hero Section -->
      <div>
        <div class="grid grid-cols-5 bg-[#2b3a56] gap-x-4 md:mx-3">
          <div class="bg-white hidden md:flex col-span-5 md:col-span-1 w-full  justify-center items-center">
            <p>For Add Section</p>
          </div>
          <div class="col-span-5 md:col-span-3 w-full px-2 md:px-0">
            <Video />
          </div>
          <div class="bg-white col-span-5 md:col-span-1 md:w-full my-4 md:my-0 mx-2 md:mx-0 flex justify-center items-center ">
            <p>For Add Section</p>
          </div>
        </div>
      </div>
<!--      Category Section -->
      <div class=" mx-3 mt-4 md:mt-8 px-3 md:px-8  inline-flex gap-x-3 md:gap-x-16 bg-gradient-to-r to-cyan-500 from-blue-500  rounded-r-2xl">
        <div v-for="(category, i) in categories" :key="i" class="">
            <button @click="toggleActive(i)" :class="isMatch===i ? 'active-button' : ''" class="text-white py-2  md:px-4  font-[600] ">{{ category.name }}</button>
        </div>
      </div>
      <!--       Channel Section -->
      <div class="grid  grid-cols-3  xl:grid-cols-5 2xl:grid-cols-7 py-6 md:py-8 gap-4 px-2 md:px-2">
        <div v-for="(channel, i) in channels" :key="i" class=" flex justify-center">
          <channel-card :channel="channel" :index="i" />
        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
const isActive = ref(false);
const isMatch = ref(0);

const categories = [
  { name:"Sports" },
  { name:"INBangla" },
  { name:"Hindi" },
  { name:"English" },
  { name:"Bangla" },
]
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

const toggleActive =(index)=> {
  isMatch.value = index
  isActive.value = !isActive.value
  console.log('ok');
}
</script>

<style  scoped>
.active-button {
  height: 100%;
  background-color: #007bff;
  color: white;
  border: none;
  cursor: pointer;
}
</style>
