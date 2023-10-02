<script setup lang="ts">
import VitoModel from './VitoModel.vue'
import ItemsKit from './ItemsKit.vue'
</script>

<template>
  <div class="AboutKit">
    <div class="bg_wall" />
    <img class="glow_blue glow_bottom" src="/img/bg/glow_bottom_blue.png" alt="" />
    <div class="separate">
      <VitoModel />
      <ItemsKit />
    </div>
  </div>
</template>

<style scoped lang="scss">
.AboutKit {
  width: 100%;
  height: max-content;
  position: relative;
  @media screen and (min-width: 1280px) {
    margin-top: 54px;
    height: 1029px;
  }
}
.bg_wall {
  background-image: url('/img/bg/background_wall.png');
  background-size: 100% 512px;
  background-position: top;
  background-repeat: no-repeat;
  width: 100%;
  height: 1024px;
  position: absolute;
  top: 0;
  left: 0;
  @media screen and (min-width: 1280px) {
    background-size: 100% 100%;
    background-position: center;
    height: 100%;
  }
}
.glow_bottom {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
}
.glow_blue {
  height: 172px;
}
.separate {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  width: 100%;
  height: 100%;
  @media screen and (min-width: 1280px) {
    gap: 160px;
    flex-direction: row;
    justify-content: center;
    align-items: flex-start;
  }
}
</style>
