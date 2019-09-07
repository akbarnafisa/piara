<template>
  <transition
    name="fade"
    mode="out-in"
  >
    <div
      v-show="currIndex === dataId"
      ref="wrapper"
      class="sliderItem flex-items"
    >
      <img
        :src="`${data}`"
        class="sliderItem__imageProduk"
        alt="Opposite Products"
        style="100%"
      >
    </div>
  </transition>
</template>

<script>
export default {
  props: {
    data: { required: true },
    type: { type: String, default: "" },
    currIndex: { type: Number, default: 0 },
    dataId: { type: Number, default: 0 }
  },
}
</script>

<style lang="scss" scoped>
.fade-enter-active {
  transition: opacity 1s ease;
}
.fade-leave-active {
  transition: opacity 0.25s ease;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.sliderItem__imageProduk {
  max-width: 212px;
  max-height: 90%;
  position: absolute;
  top: calc(50% - 30px);
  left: calc(50% + 1px);
  transform: translate3d(-50%, -50%, 0);
}
</style>