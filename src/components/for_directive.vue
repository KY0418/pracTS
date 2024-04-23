<script setup lang="ts">
import {ref,computed} from "vue"

// const cocktailListinit: string[] = ["ホワイトレディ","ブルーハワイ","ニューヨーク"]
// const cocktailListinit: {[key: number]:string} = {
//   2345: "ホワイトレディ",
//   4412: "ぶるーはわい",
//   6792:"ニューヨーク"
// }
// const cocktailListinit = new Map<number,string>();
// cocktailListinit.set(2345,"ホワイトレディ")
// cocktailListinit.set(4412,"ブルーハワイ")
// cocktailListinit.set(6792,"ニューヨーク")
// const cocktailList = cocktailListinit

// const whiteLadyInit :{
//   id : number,
//   name : string,
//   price : number,
//   recipe : string,
// } = {
//   id : 2345,
//   name : "whitelady",
//   price : 1200,
//   recipe : "ジン30ml+コワントロー15ml+レモン果汁+15ml"
// }

const cocktailDatalistInit : Cocktail[] = [
  {id:2345,name:"ホワイトレディ",price:1200},
  {id:4412,name:"ぶるーはわい",price:1500},
  {id:6792,name:"ニューヨーク",price:1100},
  {id:8429,name:"マティーニ",price:1500}
]

interface Cocktail {
  id : number,
  name: string,
  price: number,
}
const cocktailDatalist = ref(cocktailDatalistInit)
</script>

<template>
  <!-- <ul>
    <li v-for="[id,cocktailName,] in cocktailList" v-bind:key="'cocktailList' + id" >
      IDが{{id}}のカクテルは{{cocktailName}}
    </li>
  </ul>
  <ul>
    <li v-for="(cocktailName,id,index) in cocktailList" v-bind:key="'cooktaiList' + id">
      {{index}}{{ cocktailName }} (インデックス:{{ id}})
    </li>
  </ul> -->
  <!-- <dl>
    <template v-for="(value,key) in whitelady" v-bind:key="key">
      <dt>{{ key }}</dt>
      <dd>{{ value }}</dd>
    </template>
  </dl> -->
  <li v-for="cocktailItem in cocktailDatalist" v-bind:key="cocktailItem.id">
    {{ cocktailItem.name }}の値段は{{ cocktailItem.price }}

  </li>
   
</template>