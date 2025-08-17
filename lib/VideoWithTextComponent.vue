<script setup lang="ts">
import { ref, onMounted } from 'vue';
import ButtonComponent from './ButtonComponent.vue';

const props = defineProps({
    videoUrl: String,
    headerTitleTexts: Array,
    headerBodyTexts: Array,
    headerButtonText: String
})

const loadedVideo = ref("")
const translateHeadText = ref("translate-x-1/6")

function translateHead() {
    setTimeout(() => {
        translateHeadText.value = "translate-x-0"
    }, 2000)
}

onMounted(() => {
    loadedVideo.value = props.videoUrl as string

    translateHead()
})
</script>

<template>
    <div class="relative text-center overflow-hidden">
        <video preload="metadata" class="-z-10 rounded-b-4xl overflow-hidden object-cover h-200 sm:h-screen w-full"
            autoplay loop muted playsinline>
            <source v-if="loadedVideo" :src="loadedVideo" type="video/mp4" />
        </video>

        <div :class="translateHeadText"
            class="absolute inset-y-0 w-full flex flex-col place-items-start justify-center transition delay-100 duration-500 ease-in-out px-5 lg:px-10 text-white"
            style="top: 50%; left: 50%; transform: translate(-50%, -50%);">
            <div class="flex-row text-start font-bold w-full fade-up-1s">
                <h1 v-for="headerTitleText in props.headerTitleTexts">
                    {{ headerTitleText }}
                </h1>
            </div>
            <div class="flex gap-1 sm:gap-5 my-10 sm:my-20 fade-up-2s">
                <p v-for="headerBodyText in headerBodyTexts" class="sm:text-2xl">
                    {{ headerBodyText }}
                </p>
            </div>
            <ButtonComponent :text="props.headerButtonText" class="text-white" />
        </div>
    </div>
</template>