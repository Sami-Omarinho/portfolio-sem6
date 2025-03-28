<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps ({
    data: {
        type: Object,
        default: [],
    }
})

</script>

<template>
    <div class="flex">
        <div class="w-1/3 p-4"></div>
        <div class="p-16 grid grid-cols-2 gap-4 grow">
            <template v-for="tile in data">
                <div :class="{ 'bg-tertiary text-white': tile.style === 'red'}" class="shadow-md p-4 flex flex-col">
                    <h3>{{ tile.title }}</h3>
                    <span>{{ tile.description }}</span>
                </div>
            </template>
        </div>
    </div>
</template>
