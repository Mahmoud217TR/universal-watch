<script setup>

</script>
<template>
  <div class="clock relative aspect-square w-48 bg-transparent border-2 border-gray-900 rounded-full flex font-digital
      items-center justify-center text-current text-shadow-[0_0_10px] text-shadow-current shadow-black shadow-[0_0_20px]
      select-none">
    <span class="absolute top-0 start-0 w-full h-full border-transparent border-2 border-e-3 border-t-current
    border-e-current rounded-full animate-[rotate_1s_linear_infinite]"
      ></span>
      <span class="block absolute top-1/2 start-1/2 w-1/2 h-1 bg-transparent origin-left
        before:absolute before:w-4 before:aspect-square before:rounded-full before:bg-current before:-end-2 before:-top-1.5
        before:shadow-[0_0_20px_5px] before:shadow-current animate-[circleRotate_1s_linear_infinite]">
      </span>
    <span class="text-4xl">
      {{ time }}
    </span>
    <span class="spiner"></span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      now: new Date(),
      timer: null
    }
  },
  props: {
    timeZone: null,
  },
  computed: {
    time() {
      return this.now.toLocaleTimeString(undefined, {timeZone: this.timeZone, hour: "2-digit", minute: "2-digit" })
    }
  },
  mounted() {
    this.timer = setInterval(() => (this.now = new Date()), 1000)
  },
  unmounted() {
    clearInterval(this.timer)
  }
}
</script>

<style scoped>
</style>
