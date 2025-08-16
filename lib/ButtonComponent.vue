<script setup lang="ts">

const props = defineProps({
    text: String,
    link: String
})

</script>

<template>
    <a :href="props.link" class="decoration-0">
        <div
            class="font-bold text-black text-center place-content-center p-3 border-1 border-gray-400 bg-white/10 backdrop-blur-xs rounded-md hover:border-1 hover:text-white hover:bg-blue-normal transition delay-75 duration-200 ease-in cursor-pointer">
            <h4 class="text-sm lg:text-2xl">{{ props.text }}</h4>
        </div>
    </a>
</template>