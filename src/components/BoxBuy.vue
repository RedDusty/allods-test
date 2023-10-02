<template>
  <div class="BoxBuy">
    <div class="box_img">
      <img src="/img/box.png" alt="" />
    </div>
    <div class="buy_info">
      <p class="cost roboto">399 ₽</p>
      <button class="buy roboto">Приобрести</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
.BoxBuy {
  display: flex;
  column-gap: 5px;
  align-items: center;
  flex-direction: column;
  @media screen and (min-width: 640px) {
    column-gap: 35px;
    align-items: flex-end;
    flex-direction: row;
  }
}
.box_img {
  overflow: hidden;
  width: 235px;
}
.buy_info {
  padding-bottom: 63px;
}
.cost {
  font-size: 50px;
  line-height: 58px;
  color: white;
}
.buy {
  width: 180px;
  height: 40px;
  background: #fcff00;
  border: none;
  border-radius: 7px;
  color: #000000;
  font-size: 16px;
  line-height: 19px;
  text-align: center;
  cursor: pointer;
}
</style>
