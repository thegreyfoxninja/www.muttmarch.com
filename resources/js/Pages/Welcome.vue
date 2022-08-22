<script setup>
import { Head, Link } from '@inertiajs/inertia-vue3';
import Articles from '@/Components/Articles.vue';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
})
</script>

<template>
    <Head title="Welcome" />

    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 light:bg-gray-900 sm:items-center sm:pt-0">
        <div v-if="canLogin" class="hidden fixed top-0 right-0 px-6 py-4 sm:block">
            <Link v-if="$page.props.auth.user" :href="route('dashboard')" class="text-sm text-gray-700 light:text-gray-500 underline">Dashboard</Link>

            <template v-else>
                <Link :href="route('login')" class="text-sm text-gray-700 light:text-gray-500 underline">Log in</Link>

                <Link v-if="canRegister" :href="route('register')" class="ml-4 text-sm text-gray-700 light:text-gray-500 underline">Register</Link>
            </template>
        </div>

        <div class="max-w-6xl mx-auto sm:px-6 lg:px-8 sm:mt-2 mt-5">
            <div class="flex justify-center pt-8 sm:justify-start sm:pt-0">
                <img style="height: 150px;" src="/images/muttmarch-logo.png" />
            </div>

            <div class="mt-8 bg-white light:bg-gray-800 overflow-hidden shadow sm:rounded-lg">
                <div class="grid grid-cols-1">

                    <div class="p-6 border-t border-gray-200 light:border-gray-700 md:border-t-0 md:border-l">
                        <div class="sm:ml-3 lg:ml-24 sm:mr-3 lg:mr-24">
                            <Articles></Articles>
                        </div>
                    </div>

                </div>
            </div>

            <div class="flex justify-center mt-4 sm:items-center sm:justify-between">
                <div class="text-center text-sm text-gray-500 sm:text-left">
                    <div class="flex items-center">

                    </div>
                </div>

                <div class="ml-4 text-center text-sm text-gray-500 sm:text-right sm:ml-0">
                    Mutt March 2022
                </div>
            </div>
        </div>
    </div>
</template>
