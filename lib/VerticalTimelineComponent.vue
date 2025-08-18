<script setup lang="ts">
import { TimelineComponentItem } from './TimelineComponentItem.vue';

const props = defineProps({
    timelines: Array<TimelineComponentItem>
})
</script>

<template>
    <div class="sm:grid sm:grid-cols-4">
        <ol class="relative col-start-2 col-span-2 border-s border-black dark:border-gray-700">
            <li v-for="timeline in props.timelines" class="mb-10 ms-5">
                <div class="absolute z-10 w-5 h-5 bg-blue-dark border border-1-black rounded-full mt-1 -start-2.5">
                </div>
                <div class="absolute w-7 h-7 bg-white rounded-full z-0 -start-3.5">

                </div>

                <div class="grid grid-cols-1 gap-5 mb-30">
                    <div>
                        <h5 class="my-1">
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
    </div>
</template>