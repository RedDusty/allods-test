<script setup lang="ts"></script>

<template>
  <div class="boxesPreview">
    <div class="bg_sky" />
    <div class="characters">
      <img class="character character_female" src="/img/MafiaCostume_2022_2.png" alt="" />
      <img class="character character_male" src="/img/MafiaCostume_2022_3.png" alt="" />
    </div>
    <img class="glow glow_brown glow_bottom" src="/img/bg/glow_brown_bottom.png" alt="" />
    <img class="glow glow_brown glow_side glow_side_left" src="/img/bg/glow_brown.png" alt="" />
    <img class="glow glow_brown glow_side glow_side_right" src="/img/bg/glow_brown.png" alt="" />
    <img class="glow glow_boxes" src="/img/bg/glow_boxes.png" alt="" />
    <img class="glow glow_blue glow_bottom" src="/img/bg/glow_bottom_blue.png" alt="" />
    <img class="logo" src="/img/bg/logo.png" alt="" />
    <img class="boxes" src="/img/boxes.png" alt="" />
    <div class="text_container">
      <p class="text_collection roboto_cond">КОЛЛЕКЦИОННЫЕ ИЗДАНИЯ</p>
      <p class="text_description roboto">
        Побеждайте легко, побеждайте стильно с новыми коллекционными изданиями «Аллодов Онлайн»!
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.boxesPreview {
  width: 100%;
  height: 892px;
  position: relative;
  @media screen and (min-width: 640px) {
    height: 953px;
  }
}
.bg_sky {
  background-image: url('/img/bg/background_sky.png');
  background-position: top;
  background-size: cover;
  background-repeat: no-repeat;
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  @media screen and (min-width: 1280px) {
    background-size: 100% 100%;
  }
}
.characters {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
  @media screen and (min-width: 1920px) {
    justify-content: center;
  }
}
.character {
  object-fit: contain;
  width: 50%;
  bottom: 0;
  position: absolute;
  max-height: 420px;
  &_male {
    right: 0;
    width: 61%;
    object-position: bottom;
  }
  &_female {
    width: 39%;
    object-position: bottom;
  }
  @media screen and (min-width: 640px) {
    height: 876px;
    max-height: none;
    &_male {
      object-position: 135px bottom;
    }
    &_female {
      object-position: -50px bottom;
    }
  }
  @media screen and (min-width: 980px) {
    &_male {
      object-position: right bottom;
    }
    &_female {
      object-position: bottom;
    }
  }
  @media screen and (min-width: 1280px) {
    &_male {
      width: 597px;
    }
    &_female {
      width: 577px;
    }
  }
  @media screen and (min-width: 1920px) {
    &_male {
      right: auto;
      margin-left: 1100px;
    }
    &_female {
      margin-left: -1100px;
    }
  }
}
.glow {
  position: absolute;
  &_boxes {
    display: block;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    mix-blend-mode: screen;
  }
  &_brown {
    mix-blend-mode: multiply;
    height: 380px;
  }
  &_blue {
    height: 172px;
  }
  &_side {
    width: 15%;
    @media screen and (min-width: 1290px) {
      width: 462px;
    }
    height: 100%;
    top: 0;
    &_right {
      right: 0;
      transform: rotateZ(180deg);
    }
    &_left {
      left: 0;
    }
  }
  &_bottom {
    bottom: 0;
    left: 0;
    width: 100%;
  }
}
.logo {
  display: block;
  width: 100%;
  height: 348px;
  margin: 0 auto;
  position: relative;
  top: -30px;
  @media screen and (min-width: 480px) {
    width: 376px;
  }
}
.boxes {
  display: block;
  width: 100%;
  height: 393px;
  object-fit: contain;
  margin: 0 auto;
  margin-top: -150px;
  position: relative;
  @media screen and (min-width: 640px) {
    margin-top: -100px;
  }
  @media screen and (min-width: 1280px) {
    width: 766px;
    height: 525px;
  }
}
.text_container {
  position: absolute;
  bottom: 0;
  padding: 0 12px;
  padding-bottom: 25px;
  width: 100%;
  @media screen and (min-width: 480px) {
    padding-bottom: 47px;
  }
}
.text_container p {
  text-align: center;
  color: white;
}
.text_collection {
  font-size: 42px;
  line-height: 49px;
  padding-bottom: 15px;
  @media screen and (min-width: 480px) {
    padding-bottom: 25px;
  }
}
.text_description {
  font-size: 20px;
  line-height: 23px;
}
</style>
