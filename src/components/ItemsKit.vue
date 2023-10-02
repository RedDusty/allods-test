<script setup lang="ts">
import ItemKit from './ItemKit.vue'
import BoxBuy from './BoxBuy.vue'
const itemsData = [
  {
    icon: 'game_time',
    name: 'Игровое время',
    pay: '30 дней'
  },
  {
    icon: 'toolbox',
    name: 'Запечатанный набор \nинструментов',
    free: '1',
    pay: '1'
  },
  {
    icon: 'fragile_rune_pure',
    name: 'Хрупкая чистая руна \n10-й ступени',
    free: '1'
  },
  {
    icon: 'great_symbol_abundance_creator',
    name: 'Большой символ \nизобилия творца',
    free: '10'
  },
  {
    icon: 'mana_battery',
    name: 'Мана-батарея',
    pay: '20'
  },
  {
    icon: 'memory_module',
    name: 'Модуль памяти',
    pay: '10'
  },
  {
    icon: 'assistant_vito',
    name: 'Помощник Вито',
    free: '1',
    pay: '1'
  }
]
const serverType = ['Бесплатные сервера', 'Подписочный сервер']
</script>

<template>
  <div class="ItemsKit">
    <p class="kit_name roboto_cond">НАБОР «ПОСЫЛКА С КОНТРАБАНДОЙ»</p>
    <div class="items">
      <div class="server_buttons">
        <button v-for="(server, idx) in serverType" class="server_button roboto" :key="idx">
          {{ server }}
        </button>
      </div>
      <ItemKit
        v-for="(item, idx) in itemsData"
        :key="idx"
        :icon="item.icon"
        :name="item.name"
        :free="item.free"
        :pay="item.pay"
      />
    </div>
    <BoxBuy />
  </div>
</template>

<style scoped lang="scss">
.ItemsKit {
  display: flex;
  flex-direction: column;
  row-gap: 35px;
}
.kit_name {
  font-size: 30px;
  line-height: 35px;
  color: #416df4;
  text-align: center;
  padding: 0 6px;
}
.items {
  display: flex;
  flex-direction: column;
  row-gap: 1px;
}
.server_buttons {
  display: flex;
  column-gap: 11px;
  justify-content: flex-end;
  padding-bottom: 10px;
}
.server_button {
  width: 90px;
  height: auto;
  padding: 6px;
  font-size: 12px;
  line-height: 14px;
  text-align: center;
  color: #671d00;
  background-color: transparent;
  border: 1px solid #671d007a;
  border-radius: 1px;
  @media screen and (min-width: 680px) {
    width: 140px;
    height: 23px;
  }
}
</style>
