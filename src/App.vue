<script setup>
import NavBar from './components/NavBar.vue';
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';
import Portfolio from './components/Portfolio.vue';
import ContactSection from './components/ContactSection.vue';
import SiteFooter from './components/SiteFooter.vue';
</script>

<template>
    <NavBar />
    <main>
        <Hero />
        <About />
        <Services />
        <Portfolio />
        <ContactSection />
    </main>
    <SiteFooter />
</template>
