<script setup lang="ts">
import { ref, onMounted } from 'vue';

const props = defineProps({
    text: String
})

const textColor = ref("text-white")

onMounted(() => {
    window.addEventListener("scroll", () => {
        textColor.value = scrollY > window.screen.height - 200 ? "text-black" : "text-white"
    })
})

</script>

<template>
    <div :class="textColor"
        class="font-bold p-1 text-center border-0 border-gray-400 rounded-md hover:text-blue-dark hover:underline hover:underline-offset-8 transition delay-40 duration-150 ease-in-out cursor-pointer">
        <h4 class="text-sm lg:text-2xl">{{ props.text }}</h4>
    </div>
</template>