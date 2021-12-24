<template>
    <app-layout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Inventario
            </h2>
        </template>

        <div class="intro-y py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <div class="bg-gray-200 bg-opacity-25 grid grid-cols-1 md:grid-cols-4 border-t">
                        <div class="p-6 cursor-pointer transition md:border-t md:border-l border-gray-200 ">
                            <Link :href="route('categoria.index')">
                                <div class="flex flex-col items-center duration-500  hover:-translate-y-1 hover:scale-110 transform">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-chart-circles " width="100" height="100" viewBox="0 0 24 24" stroke-width="1.5" stroke="#000bfb" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                        <circle cx="9.5" cy="9.5" r="5.5" />
                                        <circle cx="14.5" cy="14.5" r="5.5" />
                                    </svg>            
                                    <div class="ml-4 text-lg text-gray-600 leading-7 font-semibold"><a href="{{ route('categoria.index') }}">Categorias</a></div>
                                </div>

                        
                            </Link>
                        </div>

                        <div class="p-6 cursor-pointer transition md:border-t md:border-l border-gray-200 ">
                            <Link :href="route('categoria.index')">
                                <div class="flex flex-col items-center duration-500  hover:-translate-y-1 hover:scale-110 transform">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-chart-circles " width="100" height="100" viewBox="0 0 24 24" stroke-width="1.5" stroke="#000bfb" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                        <circle cx="9.5" cy="9.5" r="5.5" />
                                        <circle cx="14.5" cy="14.5" r="5.5" />
                                    </svg>            
                                    <div class="ml-4 text-lg text-gray-600 leading-7 font-semibold"><a href="{{ route('categoria.index') }}">Categorias</a></div>
                                </div>

                        
                            </Link>
                        </div>

                        <div class="p-6 cursor-pointer transition md:border-t md:border-l border-gray-200 ">
                            <Link :href="route('categoria.index')">
                                <div class="flex flex-col items-center duration-500  hover:-translate-y-1 hover:scale-110 transform">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-chart-circles " width="100" height="100" viewBox="0 0 24 24" stroke-width="1.5" stroke="#000bfb" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                        <circle cx="9.5" cy="9.5" r="5.5" />
                                        <circle cx="14.5" cy="14.5" r="5.5" />
                                    </svg>            
                                    <div class="ml-4 text-lg text-gray-600 leading-7 font-semibold"><a href="{{ route('categoria.index') }}">Categorias</a></div>
                                </div>

                        
                            </Link>
                        </div>

                        <div class="p-6 cursor-pointer transition md:border-t md:border-l border-gray-200 ">
                            <Link :href="route('categoria.index')">
                                <div class="flex flex-col items-center duration-500  hover:-translate-y-1 hover:scale-110 transform">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-chart-circles " width="100" height="100" viewBox="0 0 24 24" stroke-width="1.5" stroke="#000bfb" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                        <circle cx="9.5" cy="9.5" r="5.5" />
                                        <circle cx="14.5" cy="14.5" r="5.5" />
                                    </svg>            
                                    <div class="ml-4 text-lg text-gray-600 leading-7 font-semibold"><a href="{{ route('categoria.index') }}">Categorias</a></div>
                                </div>

                        
                            </Link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </app-layout>
</template>

<script>
    import { Head, Link } from '@inertiajs/inertia-vue3'
    import { defineComponent } from 'vue'
    import AppLayout from '@/Layouts/AppLayout.vue'

    export default defineComponent({
        components: {
            AppLayout,
            Head,
            Link,
        },
    })
</script>
