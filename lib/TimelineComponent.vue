<script setup lang="ts">
import { TimelineComponentItem } from './TimelineComponentItem.vue';

const props = defineProps({
    timelines: Array<TimelineComponentItem>
})

</script>

<template>
    <div>
        <div v-for="timeline in props.timelines" class="grid grid-cols-5 sm:grid-cols-4 gap-5 items-center h-screen">
            <div class="flex col-span-2 sm:col-span-1 justify-end place-content-end">
                <div class="relative flex items-center w-30 h-30 sm:w-50 sm:h-50">
                    <div class="w-full h-full bg-blue-dark rounded-full"></div>

                    <div class="absolute text-center w-full text-wrap font-bold text-white">
                        <h4>
                            {{ timeline.startEndDate }}
                        </h4>
                    </div>
                </div>
            </div>

            <div class="col-span-3">
                <h4 class="font-bold">
                    {{ timeline.organization }}
                </h4>
                <h4 class="font-bold text-blue-light mb-5">
                    {{ timeline.position }}
                </h4>
                <h4>
                    {{ timeline.description }}
                </h4>
            </div>
        </div>
    </div>
</template>