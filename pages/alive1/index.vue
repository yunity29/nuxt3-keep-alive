<template>
    <div>
        This is Keep alive1!
        <button @click="state.counter = state.counter+1 ">count up!</button>
        <div>
            count:{{state.counter}}
        </div>
        <div style="height: 500px;"></div>
        <div style="height: 500px;"></div>
        <div style="height: 500px;"></div>
        <div style="height: 500px;">a</div>
    </div>
    
</template>
<script lang="ts" setup>
    definePageMeta({
        keepalive: true,
    });
    const state = reactive({
        counter: 0,
        scrollTop: 0,
    })

    onMounted(() => {console.log('alive1 onMounted')})
    onUnmounted(() => {console.log('alive1 onUnmounted')})
    onActivated(() => {
        console.log('alive1 onActivated')
        console.log('scroll:' + state.scrollTop)

        setTimeout(()=> {
            window.scrollTo({
                top: state.scrollTop
            })
        }, 100)

        
    })
    onDeactivated(() => {
        console.log('alive1 onDeactivated')
        state.scrollTop = window.scrollY;
    })
</script>