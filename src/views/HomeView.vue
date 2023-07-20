<template>

<div>{{ counter.count }}</div>
<div>
    <button @click="add">加</button>
</div>
<div>{{ counter.doubleCount }}</div>

</template>

<script setup lang='ts'>
import { ref, reactive } from 'vue' 
import { useCounterStore } from '@/stores/counter';
const counter = useCounterStore()
const add = ()=>{
    counter.increment()
}

</script>
<style scoped>

</style>