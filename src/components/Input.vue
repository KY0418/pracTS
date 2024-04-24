<script setup lang="ts">
import {ref} from "vue"

const inputNameModel = ref("山田太郎") 
</script>

<template>
    <input type="text" v-model="inputNameModel">
    <p>{{ inputNameModel }}</p>
</template>