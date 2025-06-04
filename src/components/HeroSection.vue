<template>
    <section class="hero-section d-flex align-items-center justify-content-center text-white text-center">
        <div data-aos="fade-up" data-aos-delay="500" class="overlay container-fluid my-5 py-5">
            <h1 class="display-4 fw-bold mt-2 py-2">{{ $t('hero_section.primary_line') }}</h1>
            <p class="lead w-50 mx-auto py-2">{{ $t('hero_section.secondary_line') }}</p>
            <a class="btn btn-join btn-lg mt-3" href="#stats">{{ $t('hero_section.join_button') }}</a>
        </div>
    </section>
</template>

<script setup>
import { onMounted } from 'vue';
import gsap from 'gsap';

onMounted(() => {
  gsap.from('.hero-content', { opacity: 0, y: -50, duration: 1 });
});
</script>

<style scoped>
.hero-section {
    height: 100vh;
    background-image: url('@/assets/hero.jpg');
    background-size: cover;
    background-position: center;
    /* position: relative; */
}

.overlay {
    height: 100%;
    background-color: rgba(0, 60, 0, 0.5);
    padding: 3rem;
    /* border-radius: 1rem; */
    color: white;
}
</style>