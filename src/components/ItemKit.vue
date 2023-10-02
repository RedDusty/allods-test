<script setup lang="ts">
const { icon, name, free, pay } = defineProps<{
  icon: string
  name: string
  free?: string
  pay?: string
}>()
const imgURL = process.env.NODE_ENV === 'development' ? '' : import.meta.env.BASE_URL
</script>

<template>
  <div class="item-container roboto">
    <img :src="imgURL + 'img/items/' + icon + '.png'" alt="" width="64" height="64" />
    <div class="item-name">{{ name }}</div>
    <p>{{ free ? free : '-' }}</p>
    <p>{{ pay ? pay : '-' }}</p>
  </div>
</template>

<style scoped lang="scss">
.item-container {
  width: 100%;
  height: auto;
  padding: 6px 1px;
  font-size: 16px;
  line-height: 19px;
  color: white;
  display: grid;
  align-items: center;
  justify-items: center;
  grid-template-columns: 64px minmax(100px, 1fr) 90px 90px;
  column-gap: 1px;
  border: 1px solid #671d007a;
  border-radius: 1px;
  @media screen and (min-width: 520px) {
    height: 74px;
    padding: 6px 1px 6px 6px;
    grid-template-columns: 64px 217px 90px 90px;
    column-gap: 10px;
  }
  @media screen and (min-width: 680px) {
    width: 632px;
    column-gap: 20px;
    grid-template-columns: 64px 247px 120px 120px;
  }
}
.item-name {
  justify-self: flex-start;
  white-space: pre-wrap;
  width: 100%;
}
</style>
