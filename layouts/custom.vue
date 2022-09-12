<template>
    <div class="layout">
        <header>
            <NuxtLink to="/alive1">to alive1</NuxtLink>
            /
            <NuxtLink to="/alive2">to alive2</NuxtLink>
            /
            <NuxtLink to="/alive-custom-layout">alive-custom-layout</NuxtLink>
        </header>
        <slot></slot>
        <header>
            <NuxtLink to="/alive1">to alive1</NuxtLink>
            /
            <NuxtLink to="/alive2">to alive2</NuxtLink>
            /
            <NuxtLink to="/alive-custom-layout">alive-custom-layout</NuxtLink>
        </header>
    </div>
</template>
<script lang="ts" setup>

    // onMounted(console.)
</script>
<style>
    .layout {
        padding: 16px;
    }
    header {
        margin: 16px 0;
    }
</style>