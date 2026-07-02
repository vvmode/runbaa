<script setup>
const services = [
    {
        title: 'Enterprise Software Development',
        desc: 'Custom web platforms and portals built on modern, maintainable architectures — from requirements through to production launch.',
    },
    {
        title: 'Secure System Integration',
        desc: 'Connecting internal systems, third-party services, and payment or logistics providers into a single reliable platform.',
    },
    {
        title: 'Digital Transformation',
        desc: 'Moving manual and paper-based workflows into structured, role-based digital systems for private and public sector clients.',
    },
    {
        title: 'Frontend & UX Engineering',
        desc: 'Responsive, accessible interfaces built with Vue 3 and Tailwind CSS, designed around real user workflows.',
    },
    {
        title: 'Backend & API Development',
        desc: 'Laravel-based APIs, database design, and business logic engineered for reliability and scale.',
    },
    {
        title: 'Security & DevSecOps',
        desc: 'Secure coding standards, SAST/DAST remediation, CI/CD pipelines, and infrastructure provisioning on DigitalOcean.',
    },
];
</script>

<template>
    <section id="services" class="bg-slate-50 py-24">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="max-w-2xl">
                <h2 class="text-sm font-semibold tracking-wide text-blue-600 uppercase">What We Do</h2>
                <p class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">Services built around the full delivery lifecycle</p>
            </div>

            <div class="mt-14 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
                <div v-for="service in services" :key="service.title"
                     class="rounded-2xl border border-slate-200 bg-white p-7 transition hover:border-blue-200 hover:shadow-sm">
                    <div class="flex h-11 w-11 items-center justify-center rounded-xl bg-blue-50 text-blue-600">
                        <svg class="h-5 w-5" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9.75 3.104v5.714a2.25 2.25 0 01-.659 1.591L5 14.5M9.75 3.104c-.251.023-.501.05-.75.082m.75-.082a24.301 24.301 0 014.5 0m0 0v5.714c0 .597.237 1.17.659 1.591L19.8 15.3M14.25 3.104c.251.023.501.05.75.082M19.8 15.3l-1.57.393A9.065 9.065 0 0112 15a9.065 9.065 0 00-6.23-.693L5 14.5m14.8.8l1.402 1.402c1.232 1.232.65 3.318-1.067 3.611A48.309 48.309 0 0112 21c-2.773 0-5.491-.235-8.135-.687-1.718-.293-2.3-2.379-1.067-3.61L5 14.5" />
                        </svg>
                    </div>
                    <h3 class="mt-5 text-lg font-semibold text-slate-900">{{ service.title }}</h3>
                    <p class="mt-2 text-sm leading-relaxed text-slate-600">{{ service.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>
