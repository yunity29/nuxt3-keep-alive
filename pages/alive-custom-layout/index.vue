<template>
    <div>
        This is Keep alive1!
        <button @click="state.counter = state.counter+1 ">count up!</button>
        <div>
            count:{{state.counter}}
        </div>
    </div>
    
</template>
<script lang="ts" setup>
    definePageMeta({
        layout: 'custom',
        keepalive: true,
    });

    const state = reactive({
        counter: 0,
    })
</script>