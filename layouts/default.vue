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
    </div>
</template>
<style>
    .layout {
        padding: 32px;
    }
    header {
        position: fixed;
        top:0
    }
</style>