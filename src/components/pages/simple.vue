<script setup lang="ts">
import { defineProps } from 'vue';
import tiles from './tiles.vue';

const props = defineProps ({
    target: {
        type: String,
        required: true,
    },
    type: {
        type: String,
        default: 'simple',
    },
    data: {
        type: Object,
        default: [],
    }
})

</script>

<template>
    <div :id="target" class="h-dvh w-full">
        <template v-if="type === 'simple'">
            <slot></slot>
        </template>

        <template v-if="type === 'tiles'">
            <tiles :data="data"/>
        </template>
    </div>
</template>
