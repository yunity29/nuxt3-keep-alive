<template>
    <div>
        counter component:{{ state.counter }}
        <button @click="state.counter = state.counter+1">Add counter</button>
    </div>
</template>
<script lang="ts" setup>
    const state = reactive({
        counter: 0,
    })
</script>