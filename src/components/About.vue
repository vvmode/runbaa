<script setup>
const stats = [
    { value: '2023', label: 'Incorporated in the Maldives' },
    { value: '5', label: 'Full-time delivery specialists' },
    { value: '6+', label: 'Platforms delivered to production' },
    { value: '100%', label: 'Projects accepted on delivery' },
];
</script>

<template>
    <section id="about" class="mx-auto max-w-7xl px-6 py-24 lg:px-8">
        <div class="grid gap-16 lg:grid-cols-2 lg:items-start">
            <div>
                <h2 class="text-sm font-semibold tracking-wide text-blue-600 uppercase">About Runbaa Tech</h2>
                <p class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">
                    A full-lifecycle delivery team, built for secure enterprise software.
                </p>
                <p class="mt-6 leading-relaxed text-slate-600">
                    Runbaa Tech was incorporated in the Republic of Maldives in 2023 under registration number
                    <span class="font-semibold text-slate-900">P00182023</span>. We specialise in enterprise
                    software development and publishing, secure system integration, and digital transformation
                    solutions for both private and public sector clients in the Maldives.
                </p>
                <p class="mt-4 leading-relaxed text-slate-600">
                    Our core delivery team covers the complete project lifecycle — from stakeholder requirements
                    and governance documentation through to design, development, security hardening, and
                    production deployment.
                </p>
            </div>

            <div class="grid grid-cols-2 gap-6">
                <div v-for="stat in stats" :key="stat.label" class="rounded-2xl border border-slate-100 bg-slate-50 p-6">
                    <p class="text-3xl font-bold text-blue-600">{{ stat.value }}</p>
                    <p class="mt-1 text-sm text-slate-600">{{ stat.label }}</p>
                </div>
            </div>
        </div>
    </section>
</template>
