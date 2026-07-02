<script setup>
const projects = [
    {
        client: 'Lotem Travels',
        title: 'Corporate Travel Platform & Content Management System',
        desc: 'A full-stack corporate travel and reservation platform (lotemtravels.com), pairing a Vue 3 + Tailwind CSS frontend with a secure Laravel backend and a bespoke CMS for destinations, media, packages, and pricing.',
        tags: ['Dynamic booking & reservation engine', 'Multi-criteria search & filtering', 'Secure auth & account dashboards'],
        meta: 'Completed in 6 months · live in production',
    },
    {
        client: 'Daphino Maldives',
        title: 'ERP Portal for Trading & Logistics',
        desc: 'A web-based ERP system with two dedicated, role-based portals — Customer and Admin — for a trading and logistics operation.',
        tags: ['Real-time shipment tracking', 'Payment & invoice management', 'Inventory & warehouse tracking', 'Reporting & analytics dashboard'],
        meta: 'Completed in 6 months · accepted in full',
    },
    {
        client: 'Foursis Pvt Ltd',
        title: 'Inventory & Order Management System',
        desc: 'An enterprise-grade system covering live multi-warehouse stock dashboards, automated alerting, and end-to-end order tracking.',
        tags: ['Automated low-stock alerting', 'Delivery scheduling & dispatch', 'Role-permission access control', 'Security & activity logging'],
        meta: 'Completed in 8 months',
    },
    {
        client: 'Anova Pvt. Ltd',
        title: 'Project Management Software',
        desc: 'A structured, multi-role project management solution for an architectural and engineering consultancy.',
        tags: ['Task assignment & progress tracking', 'Milestone & deadline management', 'Performance dashboards', 'Role & permission management'],
        meta: 'Delivered within a 90-day timeframe',
    },
    {
        client: 'Promesa',
        title: 'Corporate Website Design & Deployment',
        desc: 'The official corporate website for a professional audit and assurance firm, from UI/UX design through to post-launch support.',
        tags: ['Responsive UI/UX design', 'Content integration', 'Post-launch technical support'],
        meta: 'Delivered in 21 calendar days',
    },
    {
        client: 'Advera',
        title: 'Corporate Website Design, Development & Deployment',
        desc: 'A custom-designed corporate website with performance optimisation and hands-on go-live support.',
        tags: ['Custom UI/UX design', 'Content management implementation', 'Performance optimisation'],
        meta: 'Delivered in 30 calendar days',
    },
];
</script>

<template>
    <section id="work" class="mx-auto max-w-7xl px-6 py-24 lg:px-8">
        <div class="max-w-2xl">
            <h2 class="text-sm font-semibold tracking-wide text-blue-600 uppercase">Our Work</h2>
            <p class="mt-3 text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">A track record of on-time, production-grade delivery</p>
            <p class="mt-4 leading-relaxed text-slate-600">
                A selection of platforms Runbaa Tech has architected, built, and deployed for clients across
                travel, trading &amp; logistics, professional services, and engineering consultancy.
            </p>
        </div>

        <div class="mt-14 grid gap-8 lg:grid-cols-2">
            <div v-for="project in projects" :key="project.client" class="flex flex-col rounded-2xl border border-slate-200 p-8">
                <span class="text-xs font-semibold tracking-wide text-blue-600 uppercase">{{ project.client }}</span>
                <h3 class="mt-2 text-xl font-semibold text-slate-900">{{ project.title }}</h3>
                <p class="mt-3 flex-1 text-sm leading-relaxed text-slate-600">{{ project.desc }}</p>
                <ul class="mt-5 flex flex-wrap gap-2">
                    <li v-for="tag in project.tags" :key="tag" class="rounded-full bg-slate-100 px-3 py-1 text-xs font-medium text-slate-600">
                        {{ tag }}
                    </li>
                </ul>
                <p class="mt-5 text-xs font-medium text-slate-400">{{ project.meta }}</p>
            </div>
        </div>
    </section>
</template>
