<template>
    <section class="text-white mt-20" id="gallery" data-aos="zoom-in">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Gallery</h2>
        <div class="px-4 xl:px-16">
            <Carousel v-bind="settings" :breakpoints="breakpoints">
                <Slide v-for="image in galleryImages" :key="image.id">
                    <div class="carousel__item p-4">
                        <div class="w-full mx-auto bg-[#111a3e] shadow-lg border border-[#1f1641] p-5">
                            <div class="w-full h-64 overflow-hidden">
                                <img 
                                    :src="image.url" 
                                    :alt="image.caption" 
                                    class="w-full h-full object-cover"
                                    loading="lazy"
                                >
                            </div>
                            <p class="text-white mt-2 text-center">{{ image.caption }}</p>
                        </div>
                    </div>
                </Slide>
                <template #addons>
                    <Navigation />
                </template>
            </Carousel>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import { Carousel, Navigation, Slide } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';

// Carousel settings
const settings = ref({
    itemsToShow: 1,
    snapAlign: "center",
})

// Breakpoints
const breakpoints = ref({
    700: {
        itemsToShow: 2.5,
        snapAlign: 'center',
    },
    1024: {
        itemsToShow: 3,
        snapAlign: 'start'
    }
})

// Gallery images data
const galleryImages = ref([
    {
        id: 1,
        url: 'src/assets/photo.jpg',
        caption: 'Gallery Image 1'
    },
    {
        id: 2,
        url: 'src/assets/photo2.jpg',
        caption: 'Gallery Image 2'
    },
    {
        id: 3,
        url: 'src/assets/photo3.jpg',
        caption: 'Gallery Image 3'
    },
    {
        id: 4,
        url: 'src/assets/dark.jpg',
        caption: 'Gallery Image 4'
    },
    {
        id: 5,
        url: 'src/assets/light.jpg',
        caption: 'Gallery Image 5'
    },
])
</script>

<style>
.carousel__prev, .carousel__next {
    color: white !important;
}
</style>