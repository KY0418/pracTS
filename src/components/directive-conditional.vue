<script setup lang="ts">
import {ref,computed} from "vue"

// const randomnumber = computed(
//   ():number => {
//     return Math.round(Math.random() * 100)
//   }
// )

const showOrNot = computed(
  (): boolean => {
    const rand = Math.round(Math.random() * 100)

    let showOrNot = false

    if (rand >= 50){
      showOrNot = true
    }

    return showOrNot
  }
)
</script>

<template>
  <!-- <p>点数は{{ randomnumber }}で
    <template v-if="randomnumber >= 80">優  </template>
      <span style="color:red;">congraturation!</span>
  </p> -->
  <section>
    v-ifを利用
    <p v-if="showOrNot">条件に合致１</p>
  </section>
  <section>
    v-showを利用
    <p v-show="showOrNot">条件に合致２</p>
  </section>
</template>