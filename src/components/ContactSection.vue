<script setup>
import { reactive } from 'vue';

const form = reactive({
    name: '',
    email: '',
    company: '',
    message: '',
});

function submit() {
    const subject = `Project enquiry from ${form.name || 'website'}`;
    const body = [
        `Name: ${form.name}`,
        `Email: ${form.email}`,
        form.company ? `Organisation: ${form.company}` : null,
        '',
        form.message,
    ].filter((line) => line !== null).join('\n');

    window.location.href = `mailto:info@runbaa.tech?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
}
</script>

<template>
    <section id="contact" class="relative overflow-hidden bg-slate-900">
        <div class="absolute -top-24 right-0 h-72 w-72 rounded-full bg-blue-600/20 blur-3xl"></div>

        <div class="relative mx-auto max-w-7xl px-6 py-24 lg:px-8">
            <div class="grid gap-16 lg:grid-cols-2">
                <div>
                    <h2 class="text-sm font-semibold tracking-wide text-blue-400 uppercase">Get in Touch</h2>
                    <p class="mt-3 text-3xl font-bold tracking-tight text-white sm:text-4xl">Let's build something secure and scalable together</p>
                    <p class="mt-6 max-w-md leading-relaxed text-slate-300">
                        Tell us about your project and our team will get back to you to discuss requirements,
                        timelines, and the right approach for your organisation.
                    </p>

                    <div class="mt-10 space-y-5 text-sm">
                        <div class="flex items-center gap-3 text-slate-300">
                            <span class="flex h-9 w-9 items-center justify-center rounded-full bg-white/10 text-blue-300">
                                <svg class="h-4 w-4" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
                                </svg>
                            </span>
                            <a href="mailto:info@runbaa.tech" class="hover:text-white">info@runbaa.tech</a>
                        </div>
                        <div class="flex items-center gap-3 text-slate-300">
                            <span class="flex h-9 w-9 items-center justify-center rounded-full bg-white/10 text-blue-300">
                                <svg class="h-4 w-4" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h1.5a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106a1.125 1.125 0 00-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97a1.125 1.125 0 00.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
                                </svg>
                            </span>
                            <a href="tel:+9609870080" class="hover:text-white">+960 987 0080</a>
                        </div>
                        <div class="flex items-center gap-3 text-slate-300">
                            <span class="flex h-9 w-9 items-center justify-center rounded-full bg-white/10 text-blue-300">
                                <svg class="h-4 w-4" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
                                </svg>
                            </span>
                            <span>Republic of Maldives</span>
                        </div>
                    </div>
                </div>

                <form @submit.prevent="submit" class="rounded-2xl bg-white p-8 shadow-xl">
                    <p class="mb-6 text-sm text-slate-500">
                        Submitting opens your email client with the details below, addressed to
                        <span class="font-medium text-slate-700">info@runbaa.tech</span>.
                    </p>

                    <div class="grid gap-5 sm:grid-cols-2">
                        <div class="sm:col-span-1">
                            <label for="name" class="text-sm font-medium text-slate-700">Full name</label>
                            <input id="name" v-model="form.name" type="text" required
                                   class="mt-1.5 block w-full rounded-lg border border-slate-300 px-3.5 py-2.5 text-sm text-slate-900 focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none">
                        </div>
                        <div class="sm:col-span-1">
                            <label for="email" class="text-sm font-medium text-slate-700">Email</label>
                            <input id="email" v-model="form.email" type="email" required
                                   class="mt-1.5 block w-full rounded-lg border border-slate-300 px-3.5 py-2.5 text-sm text-slate-900 focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none">
                        </div>
                        <div class="sm:col-span-2">
                            <label for="company" class="text-sm font-medium text-slate-700">Organisation <span class="text-slate-400">(optional)</span></label>
                            <input id="company" v-model="form.company" type="text"
                                   class="mt-1.5 block w-full rounded-lg border border-slate-300 px-3.5 py-2.5 text-sm text-slate-900 focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none">
                        </div>
                        <div class="sm:col-span-2">
                            <label for="message" class="text-sm font-medium text-slate-700">How can we help?</label>
                            <textarea id="message" v-model="form.message" rows="4" required
                                      class="mt-1.5 block w-full rounded-lg border border-slate-300 px-3.5 py-2.5 text-sm text-slate-900 focus:border-blue-500 focus:ring-1 focus:ring-blue-500 focus:outline-none"></textarea>
                        </div>
                    </div>

                    <button type="submit"
                            class="mt-6 w-full rounded-lg bg-blue-600 px-5 py-3 text-sm font-semibold text-white transition hover:bg-blue-700">
                        Send Message
                    </button>
                </form>
            </div>
        </div>
    </section>
</template>
