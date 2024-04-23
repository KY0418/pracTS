<script setup lang="ts">
import {ref} from "vue";

const mousePointerX = ref(0)
const mousePointerY = ref(0)
const onImageMousemove = (event : MouseEvent): void => {
  mousePointerX.value = event.offsetX
  mousePointerY.value = event.offsetY
}
</script>

<template>
	<section>
    <img src="./assets/logo.svg" alt="VUe`s Logo" width="500" v-on:mousemove="onImageMousemove">
    <p>position of pointer: x={{ mousePointerX }},y={{ mousePointerY }}</p>
  </section>
</template>

<style>

</style>
