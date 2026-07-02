<script setup>
import { ref } from 'vue';
import Logo from './Logo.vue';

const open = ref(false);

const links = [
    { href: '#about', label: 'About' },
    { href: '#services', label: 'Services' },
    { href: '#work', label: 'Our Work' },
    { href: '#contact', label: 'Contact' },
];
</script>

<template>
    <header class="sticky top-0 z-50 border-b border-slate-100 bg-white/90 backdrop-blur">
        <div class="mx-auto flex max-w-7xl items-center justify-between px-6 py-4 lg:px-8">
            <a href="#" aria-label="Runbaa Tech home">
                <Logo />
            </a>

            <nav class="hidden items-center gap-9 text-sm font-medium text-slate-600 md:flex">
                <a v-for="link in links" :key="link.href" :href="link.href" class="transition hover:text-blue-600">
                    {{ link.label }}
                </a>
            </nav>

            <a href="#contact"
               class="hidden rounded-full bg-blue-600 px-5 py-2.5 text-sm font-semibold text-white shadow-sm shadow-blue-200 transition hover:bg-blue-700 md:inline-block">
                Start a Project
            </a>

            <button type="button" @click="open = !open"
                    class="inline-flex items-center justify-center rounded-md p-2 text-slate-600 md:hidden" aria-label="Toggle menu">
                <svg class="h-6 w-6" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5M3.75 17.25h16.5" />
                </svg>
            </button>
        </div>

        <div v-if="open" class="border-t border-slate-100 bg-white px-6 py-4 md:hidden">
            <nav class="flex flex-col gap-4 text-sm font-medium text-slate-600">
                <a v-for="link in links" :key="link.href" :href="link.href" @click="open = false" class="hover:text-blue-600">
                    {{ link.label }}
                </a>
                <a href="#contact" @click="open = false" class="mt-2 inline-block rounded-full bg-blue-600 px-5 py-2.5 text-center font-semibold text-white">
                    Start a Project
                </a>
            </nav>
        </div>
    </header>
</template>
