<template>
  <div class="card" :style="'width:' + windowWidth * 0.8 + 'px;height:'+ windowWidth * 0.81 + 'px;'">
    <template v-if="windowWidth >= 400 && windowWidth < 800">
      <template v-for="index of 100">
        <div v-if="index <= 100 - num" :key="index" class="circle" :style="'width:' + windowWidth * 0.07 + 'px;height:' + windowWidth * 0.07 + 'px;background:black'" />
        <div v-if="index > 100 - num" :key="index" class="circle" :style="'width:' + windowWidth * 0.07 + 'px;height:' + windowWidth * 0.07 + 'px;background:' + circleColor" />
      </template>
    </template>
    <template v-if="windowWidth >= 800">
      <template v-for="index of 100">
        <div v-if="index <= 100 - num" :key="index" class="circle" :style="'width:' + windowWidth * 0.07 + 'px;height:' + windowWidth * 0.07 + 'px;background:black'" />
        <div v-if="index > 100 - num" :key="index" class="circle" :style="'width:' + windowWidth * 0.07 + 'px;height:' + windowWidth * 0.07 + 'px;background:' + circleColor" />
      </template>
    </template>
    <template v-if="windowWidth < 400">
      <template v-for="index of 100">
        <div v-if="index <= 100 - num" :key="index" class="circle" :style="'width:' + windowWidth * 0.063 + 'px;height:' + windowWidth * 0.063 + 'px;background:black'" />
        <div v-if="index > 100 - num" :key="index" class="circle" :style="'width:' + windowWidth * 0.063 + 'px;height:' + windowWidth * 0.063 + 'px;background:' + circleColor" />
      </template>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      windowWidth: 340,
      windowHeight: 800,
      circleColor: 'rgb(25, 19, 215)',
      num: 12
    }
  },
  created() {
    console.log(this.windowWidth)
    console.log(this.windowHeight)
  }
}
</script>

<style scoped>
    .card {
      max-width: 911px;
      max-height: 911px;
      background: rgb(239, 239, 239);
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
    }
    .circle {
      max-width: 81px;
      max-height: 81px;
      background: rgb(25, 19, 215);
      margin-left: 2px;
      margin-right: 2px;
      border-radius: 50%;
    }
</style>
