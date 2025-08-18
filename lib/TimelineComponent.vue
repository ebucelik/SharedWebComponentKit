<script setup lang="ts">
import { onMounted, ref } from 'vue';
import { TimelineComponentItem } from './TimelineComponentItem.vue';

const props = defineProps({
    timelines: Array<TimelineComponentItem>
})
</script>

<template>
    <div class="sm:grid sm:grid-cols-3">
        <ol class="relative col-start-2 border-s border-black dark:border-gray-700">
            <li v-for="timeline in props.timelines" class="mb-10 ms-5">
                <div class="absolute w-5 h-5 bg-blue-dark border border-1-black rounded-full -start-2.5"></div>

                <div class="grid grid-cols-1 gap-5 mb-30">
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
    </div>
</template>