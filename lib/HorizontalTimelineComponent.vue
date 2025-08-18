<script setup lang="ts">
import { TimelineComponentItem } from './TimelineComponentItem.vue';
import VerticalTimelineComponent from './VerticalTimelineComponent.vue';

const props = defineProps({
    timelines: Array<TimelineComponentItem>
})
</script>

<template>
    <div>
        <ol class="items-center hidden sm:flex">
            <li v-for="timeline in props.timelines" class="mb-6 sm:mb-0">
                <div class="flex items-center">
                    <div
                        class="z-10 flex items-center justify-center w-5 h-5 mx-1 bg-blue-dark border border-1-black rounded-full">
                    </div>
                    <div class="sm:flex w-full h-0.5 bg-black/40"></div>
                </div>
                <div class="grid grid-cols-1 gap-5 mt-1.5 mb-30">
                    <div>
                        <h5 class="mb-1">
                            {{ timeline.startEndDate }}
                        </h5>
                        <h4 class="font-bold">
                            {{ timeline.organization }}
                        </h4>
                        <h4 class="font-bold text-blue-dark mb-5">
                            {{ timeline.position }}
                        </h4>
                        <p class="text-gray-500">
                            {{ timeline.description }}
                        </p>
                    </div>
                </div>
            </li>
        </ol>

        <VerticalTimelineComponent v-bind:timelines="timelines" class="sm:hidden" />
    </div>
</template>