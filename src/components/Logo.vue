<script setup>
defineProps({
    light: { type: Boolean, default: false },
});
</script>

<template>
    <div class="flex items-center gap-2.5">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <defs>
                <linearGradient id="runbaa-mark" x1="10" y1="10" x2="90" y2="90" gradientUnits="userSpaceOnUse">
                    <stop offset="0" stop-color="#5EA8F0" />
                    <stop offset="1" stop-color="#1D4ED8" />
                </linearGradient>
            </defs>
            <path d="M20 12 H52 C68 12 78 22 78 37 C78 49 71 58 59 61 L80 88 H58 L40 63 V88 H20 V40 L38 24 H24 Z" fill="url(#runbaa-mark)" />
            <path d="M20 40 L38 24 H24 L20 30 Z" fill="#0F172A" opacity="0.25" />
        </svg>
        <span class="flex items-baseline gap-1.5 font-bold tracking-tight">
            <span class="text-lg" :class="light ? 'text-white' : 'text-slate-900'">Runbaa</span>
            <span class="text-lg text-blue-500">Tech</span>
        </span>
    </div>
</template>
