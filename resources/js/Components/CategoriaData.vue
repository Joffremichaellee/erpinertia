<template>
                                        <table id="table_id" class="table table-report -mt-2">
                                            <thead>
                                                <tr>
                                                    <th class="uppercase whitespace-nowrap">Imagen</th>
                                                    <th class="uppercase whitespace-nowrap">Categoria</th>
                                                    <th class="uppercase text-center whitespace-nowrap">Descripcion</th>
                                                    <th class="uppercase text-center whitespace-nowrap">Estado</th>
                                                    <th class="uppercase text-center whitespace-nowrap">Acciones</th>
                                                </tr>
                                            </thead>
                                            <tbody>
                                                <tr v-for="categoria in categorias" :key="categoria.id" class="intro-x">
                                                    <td class="w-10">
                                                        <div class="flex justify-center">
                                                            <!--<div class="w-10 h-10 image-fit zoom-in">
                                                                <img alt="Tinker Tailwind HTML Admin Template" class="tooltip rounded-full" src="dist/images/preview-11.jpg" title="Uploaded at 23 December 2022">
                                                            </div>-->
                                                            <div class="w-10 h-10 image-fit zoom-in">
                                                                <img alt="Tinker Tailwind HTML Admin Template" class="tooltip rounded-full" src="dist/images/preview-10.jpg" title="Uploaded at 23 December 2022">
                                                            </div>
                                                            <!--<div class="w-10 h-10 image-fit zoom-in -ml-5">
                                                                <img alt="Tinker Tailwind HTML Admin Template" class="tooltip rounded-full" src="dist/images/preview-3.jpg" title="Uploaded at 23 December 2022">
                                                            </div>-->
                                                        </div>
                                                    </td>
                                                    <td>
                                                        <!--<a href="" class="font-medium whitespace-nowrap">{{ $categoria->nombre }}</a>-->
                                                        <div class="font-medium whitespace-nowrap">{{ categoria.nombre }}</div><!--&amp;-->
                                                    </td>
                                                    <td class="text-center">{{ categoria.descripcion }}</td>
                                                    
                                                    

                                                    <td class="w-40 text-center">
                                                        
                                                        <button v-if="categoria.estado === 1" class="btn btn-success text-white btn w-12 h-5 text-xs mx-auto">  Activo </button>
                                                        
                                                        <button v-else-if="categoria.estado === 0" class="btn btn-danger text-white btn w-20 h-5 text-xs mx-auto">  Desactivado </button>
                                                        
                                                        
                                                    </td>

                                                    <td class=" text-center">
                                                        <div class="flex justify-center items-center inline-flex " >
                                                            <Link :href="route('categoria.edit', { categoria: categoria })" class="flex items-center mr-3" href="javascript:;"><!--href="javascript:;"-->
                                                                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-edit" width="14" height="14" viewBox="0 0 24 24" stroke-width="1.5" stroke="#000" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                                    <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                                                    <path d="M9 7h-3a2 2 0 0 0 -2 2v9a2 2 0 0 0 2 2h9a2 2 0 0 0 2 -2v-3" />
                                                                    <path d="M9 15h3l8.5 -8.5a1.5 1.5 0 0 0 -3 -3l-8.5 8.5v3" />
                                                                    <line x1="16" y1="5" x2="19" y2="8" />
                                                                </svg>Edit
                                                            </Link>
                                                            <!--<button type="button" @click="EliminarCategoria(categoria)">
                                                            
                                                                <button class="flex items-center text-theme-21 text-red-500">
                                                                        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-trash text-red-500" width="14" height="14" viewBox="0 0 24 24" stroke-width="1.5" stroke="#FF2C16" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                                            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                                                            <line x1="4" y1="7" x2="20" y2="7" />
                                                                            <line x1="10" y1="11" x2="10" y2="17" />
                                                                            <line x1="14" y1="11" x2="14" y2="17" />
                                                                            <path d="M5 7l1 12a2 2 0 0 0 2 2h8a2 2 0 0 0 2 -2l1 -12" />
                                                                            <path d="M9 7v-3a1 1 0 0 1 1 -1h4a1 1 0 0 1 1 1v3" />
                                                                        </svg> Delete 
                                                                </button>

                                                            </button>-->

                                                            <Link method="DELETE" :href="route('categoria.destroy', { categoria: categoria })">

                                                                <div class="flex items-center text-theme-21 text-red-500">
                                                                        <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-trash text-red-500" width="14" height="14" viewBox="0 0 24 24" stroke-width="1.5" stroke="#FF2C16" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                                                            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                                                            <line x1="4" y1="7" x2="20" y2="7" />
                                                                            <line x1="10" y1="11" x2="10" y2="17" />
                                                                            <line x1="14" y1="11" x2="14" y2="17" />
                                                                            <path d="M5 7l1 12a2 2 0 0 0 2 2h8a2 2 0 0 0 2 -2l1 -12" />
                                                                            <path d="M9 7v-3a1 1 0 0 1 1 -1h4a1 1 0 0 1 1 1v3" />
                                                                        </svg> Delete 
                                                                </div>

                                                            </Link>

                                                        </div>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
</template>
<script>

    import { Head, Link } from '@inertiajs/inertia-vue3'
    import { defineComponent } from 'vue'
    import AppLayout from '@/Layouts/AppLayout.vue'

export default defineComponent({
        
        data() {
            return {
                id: 0,
                
            }
        },
        props:['categorias'],
        components: {
            AppLayout,
            Head,
            Link,
        },
        methods: {
            
           
        }
    })
</script>
<style lang="">
    
</style>
