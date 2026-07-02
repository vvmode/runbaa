<script setup>
import Logo from './Logo.vue';

const year = new Date().getFullYear();
</script>

<template>
    <footer class="border-t border-slate-800 bg-slate-900 text-slate-300">
        <div class="mx-auto max-w-7xl px-6 py-14 lg:px-8">
            <div class="grid gap-12 md:grid-cols-4">
                <div class="md:col-span-2">
                    <Logo light />
                    <p class="mt-4 max-w-sm text-sm leading-relaxed text-slate-400">
                        Runbaa Tech is a Maldivian software development and publishing company delivering
                        enterprise software, secure system integration, and digital transformation solutions for
                        private and public sector clients.
                    </p>
                    <p class="mt-4 text-xs text-slate-500">Incorporated in the Republic of Maldives, 2023 &middot; Registration No. P00182023</p>
                </div>

                <div>
                    <h3 class="text-sm font-semibold text-white">Company</h3>
                    <ul class="mt-4 space-y-3 text-sm text-slate-400">
                        <li><a href="#about" class="hover:text-blue-400">About Us</a></li>
                        <li><a href="#services" class="hover:text-blue-400">Services</a></li>
                        <li><a href="#work" class="hover:text-blue-400">Our Work</a></li>
                    </ul>
                </div>

                <div>
                    <h3 class="text-sm font-semibold text-white">Contact</h3>
                    <ul class="mt-4 space-y-3 text-sm text-slate-400">
                        <li>
                            <a href="mailto:info@runbaa.tech" class="hover:text-blue-400">info@runbaa.tech</a>
                        </li>
                        <li>
                            <a href="tel:+9609870080" class="hover:text-blue-400">+960 987 0080</a>
                        </li>
                        <li>Republic of Maldives</li>
                    </ul>
                </div>
            </div>

            <div class="mt-12 flex flex-col items-center justify-between gap-4 border-t border-slate-800 pt-8 text-xs text-slate-500 md:flex-row">
                <p>&copy; {{ year }} Runbaa Tech. All rights reserved.</p>
                <p>Code. Innovate. Elevate.</p>
            </div>
        </div>
    </footer>
</template>
