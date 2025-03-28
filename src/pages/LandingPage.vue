<script setup lang="ts">
import { onMounted, useTemplateRef } from 'vue';
import { gsap } from "gsap";
import simple from '../components/pages/simple.vue';
import tiles from '../js/tilesProjects';

const header = useTemplateRef('landing_header');
const getStarted = useTemplateRef('getStarted');

onMounted(() => {
    gsap.fromTo(header.value, { y:135 }, { y:0, delay:0.5 });
    gsap.fromTo(getStarted.value, { y:10 }, { 
        y:0,
        ease: "sine.out",
        repeat:-1,
        duration:1, 
        yoyo: true,
    })
})

</script>

<template>
    <div class="flex flex-col gap-8 grow justify-center items-center h-screen font-exo">
        <div class="px-5 pb-5">
            <h1 ref="landing_header" class="text-[8rem] uppercase h1_title mb-0 mt-[-10rem] z-0">
                Portfolio
            </h1>
            <div class="flex bg-tertiary w-full h-full p-4 z-10 relative items-center">
                <h3 class="text-white text-2xl h-fit">Omar Kacimi - Semester 6</h3>
            </div>
        </div>
        <a href="#projects" class="next_button flex items-center gap-2">Get started <i ref="getStarted" class="pi pi-arrow-down text-secondary"></i></a>
    </div>

    <simple target="projects" type="tiles" :data="tiles"/>
    
</template>
