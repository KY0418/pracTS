<script setup lang="ts">
import {ref} from "vue"
import OneInfo from "./components/OneInfo.vue";

const weatherlistInit = new Map<number,Weather>()
weatherlistInit.set(1,{id: 1,title: "今日の天気",content:"今日は一日中晴れでしょう"})
weatherlistInit.set(2,{id: 2,title: "明日の天気",content:"明日は一日中雨でしょう"})
weatherlistInit.set(3,{id: 3,title: "明後日の天気",content:"明後日は一日中雪でしょう"})

const weatherlist = weatherlistInit
interface Weather {
	id: number
	title: string
	content: string
}
</script>

<template>
	<h1>Props基礎</h1>
	<section>
		<h2>ループでコンポーネントを作成</h2>
		<OneInfo 
			v-for="[id,weather] in weatherlist"
			v-bind:key="id"
			v-bind:title="weather.title"
			v-bind:content="weather.content"/>
		<WithModel />
	</section>
</template>

<!-- <style>
section {
	border: blue 1px solid;
	margin: 10px;
}
</style> -->