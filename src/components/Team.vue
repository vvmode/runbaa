<script setup>
const team = [
    { role: 'Project Manager / Requirements Engineer', desc: 'Stakeholder coordination, requirements elicitation, and governance gate documentation.' },
    { role: 'Frontend Developer', desc: 'Vue 3 user interface and UX implementation.' },
    { role: 'Backend Developer', desc: 'Laravel API, database design, and business logic.' },
    { role: 'Security Lead', desc: 'Secure coding standards, SAST/DAST remediation, and compliance with the MDS Secure Software Development Standard.' },
    { role: 'DevSecOps Engineer', desc: 'CI/CD pipelines, infrastructure provisioning, and deployment on DigitalOcean.' },
];
</script>

<template>
    <section id="team" class="bg-slate-50 py-24">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="max-w-2xl">
                <h2 class="text-sm font-semibold tracking-wide text-blue-600 uppercase">Our Team</h2>
                <p class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">Five specialists, covering the entire project lifecycle</p>
            </div>

            <div class="mt-14 grid gap-6 sm:grid-cols-2 lg:grid-cols-5">
                <div v-for="member in team" :key="member.role" class="rounded-2xl border border-slate-200 bg-white p-6">
                    <div class="flex h-10 w-10 items-center justify-center rounded-full bg-gradient-to-br from-blue-400 to-blue-700 text-sm font-bold text-white">
                        {{ member.role.charAt(0) }}
                    </div>
                    <h3 class="mt-4 text-sm font-semibold text-slate-900">{{ member.role }}</h3>
                    <p class="mt-2 text-xs leading-relaxed text-slate-600">{{ member.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>
