<script setup lang="ts">
import { onMounted } from 'vue';
import anime from 'animejs';


onMounted(() => {
    anime({
        targets: '.next_button',
        duration: 4000,
        translateX: 250
    });
})

</script>

<template>
    <div class="flex flex-col gap-4 grow justify-center items-center h-screen font-exo">
        <div class="bg-tertiary px-5 pb-5">
            <h1 class="text-[8rem] uppercase h1_title mb-0 mt-[-10rem]">
                Portfolio
            </h1>
            <div class="flex">
                <h3 class="text-white text-2xl">Omar Kacimi - Semester 6</h3>
            </div>
        </div>
        <a class="next_button flex items-center gap-2">Get started <i class="pi pi-arrow-down text-secondary"></i></a>
    </div>
</template>
