<template>
    <div class="max-full">
        <nav class="bg-gray-200 max-w-full">
            <div class="mx-auto px-2 sm:px-6 lg:px-8">
                <div class="relative max-w-full flex items-center justify-between h-16">
                <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
                    <!-- Mobile menu button-->
                    <button class="inline-flex items-center justify-center p-2 rounded-md text-gray-600 hover:text-white hover:bg-gray-600 focus:outline-none focus:bg-gray-600 focus:text-white transition duration-150 ease-in-out" aria-label="Main menu" aria-expanded="false">
                    <!-- Icon when menu is closed. -->
                    <!-- Menu open: "hidden", Menu closed: "block" -->
                    <svg v-on:click="toggleMenu" v-bind:class="{block: isOpen, hidden: !isOpen}" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>
                    <!-- Icon when menu is open. -->
                    <!-- Menu open: "block", Menu closed: "hidden" -->
                    <svg v-on:click="toggleMenu" v-bind:class="{block: !isOpen, hidden: isOpen}"  class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                    </button>
                </div>
                <div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
                    <div class="flex-shrink-0">
                    <img class="block lg:hidden h-8 w-auto" src="https://tailwindui.com/img/logos/workflow-mark-on-dark.svg" alt="Workflow logo">
                    <img class="hidden lg:block h-8 w-auto" src="https://tailwindui.com/img/logos/workflow-logo-on-dark.svg" alt="Workflow logo">
                    </div>
                    <div class="hidden sm:block sm:ml-6">
                    <div class="flex">
                        <a href="/" class="px-3 py-2 rounded-md text-sm font-medium leading-5 text-white bg-gray-400 focus:outline-none focus:text-white focus:bg-gray-600 transition duration-150 ease-in-out">Home</a>
                        <a href="/blog" class="ml-4 px-3 py-2 rounded-md text-sm font-medium leading-5 text-gray-600 hover:text-white hover:bg-gray-600 focus:outline-none focus:text-white focus:bg-gray-600 transition duration-150 ease-in-out">Blog</a>
                        <a href="/about" class="ml-4 px-3 py-2 rounded-md text-sm font-medium leading-5 text-gray-600 hover:text-white hover:bg-gray-600 focus:outline-none focus:text-white focus:bg-gray-600 transition duration-150 ease-in-out">About</a>
                    </div>
                    </div>
                </div>
                </div>
            </div>

            <!--
                Mobile menu, toggle classes based on menu state.

                Menu open: "block", Menu closed: "hidden"
            -->
            <div v-on:click="toggleMenu" v-bind:class="{block: !isOpen, hidden: isOpen}"  class=" sm:hidden">
                <div class="px-2 pt-2 pb-3">
                <a href="/" class="block px-3 py-2 rounded-md text-base font-medium text-white bg-gray-400 focus:outline-none focus:text-white focus:bg-gray-600 transition duration-150 ease-in-out">Home</a>
                <a href="/blog" class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-600 hover:text-white hover:bg-gray-600 focus:outline-none focus:text-white focus:bg-gray-600 transition duration-150 ease-in-out">Blog</a>
                <a href="/about" class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-600 hover:text-white hover:bg-gray-600 focus:outline-none focus:text-white focus:bg-gray-600 transition duration-150 ease-in-out">About</a>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    data () {
        return {
            isOpen: true
        }
    },
    methods: {
        toggleMenu: function toggleMenu() {
            this.isOpen = !this.isOpen;
        }
    } 
}
</script>
