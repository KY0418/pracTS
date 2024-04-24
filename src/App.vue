<script setup lang="ts">
import { provide, ref} from "vue";
import Input from "./components/Input.vue";
import Select from "./components/Select.vue";
import Radio from "./components/Radio.vue";

const CurrentComp = ref(Input)

const CurrentCompName = ref("Input")

const compList = [Input,Radio,Select]
const compNameList: string[] = ["Input","Radio","Select"]

let CurrentCompIndex = 0
const switchComp = (): void => {
	CurrentCompIndex++

	if(CurrentCompIndex >= 3){
		CurrentCompIndex = 0
	}

	CurrentComp.value = compList[CurrentCompIndex]

	CurrentCompName.value = compNameList[CurrentCompIndex]

}
</script>

<template>
	
</template>
