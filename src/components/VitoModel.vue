<template>
  <div class="VitoModel">
    <div class="glow_vito" />
    <img src="/img/Vito_model.png" alt="" />
  </div>
</template>

<style scoped lang="scss">
.VitoModel {
  width: 100%;
  height: max-content;
  position: relative;
  @media screen and (min-width: 640px) {
    width: 441px;
  }
  @media screen and (min-width: 1280px) {
    height: 891px;
  }
}
.glow_vito {
  position: absolute;
  width: 100%;
  height: 486px;
  margin-left: 0;
  margin-top: 0;
  border-radius: 686px;
  mix-blend-mode: lighten;
  opacity: 20%;
  background: #416df4;
  filter: blur(100px);
  @media screen and (min-width: 1280px) {
    margin-left: -70px;
    margin-top: 160px;
    width: 680px;
    height: 686px;
  }
}

.VitoModel img {
  width: 100%;
  height: 386px;
  object-fit: contain;
  object-position: center;
  position: relative;
  @media screen and (min-width: 1280px) {
    height: 441px;
    height: 891px;
  }
}
</style>
